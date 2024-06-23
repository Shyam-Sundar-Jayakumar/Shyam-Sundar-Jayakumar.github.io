An Unmanned Aerial Vehicle configuration integrated with tilting mechanism of the rotors for forward flight for efficiency, and wing folding mechanism for the wings for compact storage

_Design of the mechanism_

| | | |
|-|-|-|
|![VTOL](tilt-wing/VTOL.jpg)|![transition](tilt-wing/transition.jpg)|![fixedwing](tilt-wing/fixedwing.jpg)|

---

##### Goal of this project

* To design and develop a UAV configuration compatible with efficient flight and compact storage
* Component selection for the servo motors, which need to produce enough torque to tilt and fold the rotors and wings respectively
* Estimation of gear dimensions to produce a smooth transition between the initial and final stages.
* Assembly of gears with the rotors and sample wings to validate the component selection

---

##### Motivation

Efficiency of an UAV is always been a concern not alone for its flight, but also for its storage. This was the intial spark for this unique configuration of the tiltable and foldable mecahism, which can provide the capablities of efficient flight during VTOL and fixed wing phase; and the wings can be folded for compact storage when not in flight.

---

##### Research process

The following methodology is used to design and develop the tilting and folding mechanism of the UAV

_Generation of CAD models of the mechanism_

Initially, with the estimated design parameters, a preliminary model of the mechanisms were modelled using CATIA.

  ![cubehandle](bmv/cubehandle_3.png)
  _Object in wireframe mode with normals_

_Estimation of gear dimesnsions and production_

Gears play the crucial role in the mechanisms. Their dimensions were estimated with respect to the gear ratios 

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
