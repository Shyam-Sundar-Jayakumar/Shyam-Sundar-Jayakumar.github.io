A unique fixed wing configured UAV, with the capablities of tilting its wing to transition between fixed wing and multirotor configuration with respect to its mission profile

Source code: @ [github repository](https://github.com/acrlakshman/BasicModelViewer)

_Design of the UAV_

| | | |
|-|-|-|
|![VTOL](bmv/VTOL.jpg)|![transition](bmv/transition.jpg)|![fixedwing](bmv/fixedwing.jpg)|

---

##### Goal of this project

* To design and develop a effiecient fixed wing UAV capable of performing vertical take off and landing using CATIA.
* To estimate the design parameters of the UAV such as wing span, propeller dimension.
* Computational analysis of the components to validate their outcomes such as thrust and lift production.
* Component selection was carried out to select the appropriate components required to fulfil the requirements of the mission
* Design of altitude controller to ensure the vertical stability of the UAV using MATLAB Simulink.

---

##### Motivation

Fixed wing UAVs are capable of providing a efficient flight in mid air and multi rotor UAVs gives the ability of vertical take-off and Landing. This lured my attention towards VTOL UAVs. Instead of going with the conventional VTOL configuration, I was keen to experiment on tilt wing UAVs, which has the ability to transition between multi rotor mode and fixed wing mode. As these complex configurations require stability, the process was pushed towards modelling altitude and attitude controllers for the UAV

---

##### Research process

The following methodology is used to design and analyse the performance of the tiltwing UAV

_surface model of propellers_

```sh
git clone https://github.com/acrlakshman/BasicModelViewer.git BasicModelViewer
cd BasicModelViewer
mkdir build
cd build
qmake ..
make
```

_Demo_

Currently GUI for _Basic Model Viewer_ is not complete, hence for the time being `RenderScene.cpp` & `RenderScene.h` are provided to render a scene. This essentially forces user to write code for what he is looking to visualize.

* Initialize the RenderObj object as follows in the function `InitializeScene`

  ```cpp
  if (!this->render_obj.LocalInitialize("../Resources/cubehandle0fix.obj"))
    return false;
  ```

  Assuming the object of RenderObj is called in the Draw function, the following scene is being rendered in the graphics window (zoom towards the object by scrolling mouse wheel)

  ![cubehandle](bmv/cubehandle_1.png)
  _Thanks to [Pradeep Garigipati] for providing OBJ file of this object_

* To get the camera details, _`press c on the keyboard`_, this saves the details in a file `scene_details.txt` in the parent directory. Sample output is as follows

  ```sh
  Camera details (Right handed system)
  Camera position: (36.402737, 41.488392, 30.879433)
  Camera look at: (0.000000, 0.000000, 0.000000)
  Camera up vector: (-0.493296, 0.754725, -0.432489)
  Camera field of view: 23.000000

  Camera details (Left handed system)
  Camera position: (36.402737, 41.488392, -30.879433)
  Camera look at: (0.000000, 0.000000, 0.000000)
  Camera up vector: (-0.493296, 0.754725, 0.432489)
  Camera field of view: 23.000000

  Light details (Right handed system)
  Light position: (0.000000, 0.000000, 10.000000)

  Light details (Left handed system)
  Light position: (0.000000, 0.000000, -10.000000)
  ```

* To show the surface mesh of the object (wireframe), update the `InitializeScene` function as follows

  ```cpp
  if (!this->render_obj.LocalInitialize("../Resources/cubehandle0fix.obj"))
    return false;
  this->render_obj.show_wire_frame(true);
  ```

  ![cubehandle](bmv/cubehandle_2.png)
  _wireframe mode_

* Let us show the normals on the surface mesh of the object, by updating the `InitializeScene` function as follows

  ```cpp
  if (!this->render_obj.LocalInitialize("../Resources/cubehandle0fix.obj"))
    return false;
  this->render_obj.show_wire_frame(true);
  this->render_obj.show_normals(true);
  ```

  ![cubehandle](bmv/cubehandle_3.png)
  _Object in wireframe mode with normals_

  > Note: Normals do not scale properly with the object dimensions. Hence for now, in case of the objects with small dimensional values, user needs to manually edit the size of normals (e.g. Change the value of `normal_scalar` in `GenericObject.cpp`)

* The following modification shows two objects with different light settings

  In `InitializeScene` function:

  ```cpp
  if (!this->cubehandle_obj.LocalInitialize("../Resources/cubehandle0fix.obj"))
    return false;
  this->cubehandle_obj.show_wire_frame(false);
  this->cubehandle_obj.show_normals(false);

  if (!this->teapot_obj.LocalInitialize("../Resources/teapot.obj"))
    return false;

  Light light_for_teapot;
  light_for_teapot.position = QVector3D(0.0, 0.0, 10.0);
  light_for_teapot.color_ambient = QVector3D(0.75, 0.6, 0.5);
  light_for_teapot.color_diffuse = QVector3D(0.75, 0.6, 0.5);
  light_for_teapot.color_specular = QVector3D(1.0, 1.0, 1.0);

  this->teapot_obj.EditLight(light_for_teapot);

  this->teapot_obj.show_wire_frame(false);
  this->teapot_obj.show_normals(false);
  ```

  In `Draw` function

  ```cpp
  if (!this->cubehandle_obj.Draw(projection, modelview_cam, modelview, shader_))
    return false;

  modelview.translate(QVector3D(5.0, 5.0,-2.0));
  if (!this->teapot_obj.Draw(projection, modelview_cam, modelview, shader_))
    return false;
  ```

  In `TakeDown` function

  ```cpp
  this->cubehandle_obj.TakeDown();
  this->teapot_obj.TakeDown();
  ```

  ![cubehandle](bmv/cubehandle_teapot.png)

* Some default shaders are available in the folder `Shaders`.
* Texture mapping is under development.

---

##### Acknowledgements

* [Hammad Mazhar] both for helping me to understand the basics of computer graphics and for providing his camera class, the basic functionalities of which are used in this project.
* [Syoyo Fujita] for his obj file loader, which I got through Hammad.
* [Pradeep Garigipati] for providing sample obj files.
* [Andrew Seidl]

[Pradeep Garigipati]: https://pradeepgarigipati.com/
[Hammad Mazhar]: https://github.com/hmazhar
[Syoyo Fujita]: https://github.com/syoyo
[Andrew Seidl]: https://github.com/andrewseidl
