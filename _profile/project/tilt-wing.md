A unique fixed wing configured UAV, with the capablities of tilting its wing to transition between fixed wing and multirotor configuration with respect to its mission profile



_Design of the UAV_

| | | |
|-|-|-|
|![VTOL](tilt-wing/VTOL.jpg)|![transition](tilt-wing/transition.jpg)|![fixedwing](tilt-wing/fixedwing.jpg)|

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

With the general formulae to estimate the dimensions of the propeller such as pitch and chord length, the geometry of the vertical and forward propeller model were generated using CATIA.

  ![cubehandle](bmv/cubehandle_3.png)
  _Object in wireframe mode with normals_

_computational analysis of the modelled propeller_

With the surface geometry of the propellers, computational model for the propellers to proceed for simulations were generated. With the model, the thrust produced by the propellers were validated with the existing [experiment datasheet]

  ![cubehandle](bmv/cubehandle_3.png)
  _Object in wireframe mode with normals_

Entire UAV geometry was assembled with all the componenets such as wings, fuselage and propellers to perform simulations using moving reference frames for the propellers using Ansys.

  ![cubehandle](bmv/cubehandle_1.png)
  _Thanks to [Pradeep Garigipati] for providing OBJ file of this object_

* To get the camera details, _`press c on the keyboard`_, this saves the details in a file `scene_details.txt` in the parent directory. Sample output is as follows

* To show the surface mesh of the object (wireframe), update the `InitializeScene` function as follows

  ![cubehandle](bmv/cubehandle_2.png)
  _wireframe mode_

* Let us show the normals on the surface mesh of the object, by updating the `InitializeScene` function as follows

  ![cubehandle](bmv/cubehandle_3.png)
  _Object in wireframe mode with normals_

  > Note: Normals do not scale properly with the object dimensions. Hence for now, in case of the objects with small dimensional values, user needs to manually edit the size of normals (e.g. Change the value of `normal_scalar` in `GenericObject.cpp`)

* The following modification shows two objects with different light settings

  In `InitializeScene` function:

  In `Draw` function

  In `TakeDown` function


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
[experiment datasheet]: https://store.tmotor.com/product/v505-vtol-motor.html
