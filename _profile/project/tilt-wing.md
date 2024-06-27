A unique fixed wing configured UAV, with the capablities of tilting its wing to transition between fixed wing and multirotor configuration with respect to its mission profile.


_Design of the UAV_

| | | |
|-|-|-|
|![VTOL](tilt-wing/VTOL.jpg)|![transition](tilt-wing/transition.jpg)|![fixedwing](tilt-wing/fixedwing.jpg)|

_UAV during VTOL_                 _UAV during transition_                _UAV during forward flight_
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

* With the general formulae to estimate the dimensions of the propeller such as pitch and chord length, the geometry of the vertical and forward propeller model were generated using [CATIA].

| | |
|-|-|
|![VProp](tilt-wing/VProp.jpg)|![FProp](tilt-wing/FProp.jpg)|

 _Vertical propeller_             _Forward propeller_ 

_computational analysis of the modelled propeller_

* With the surface geometry of the propellers, computational model for the propellers to proceed for simulations were generated. With the model, the thrust produced by the propellers were validated with the existing [experiment datasheet]

| | |
|-|-|
|![thrust](tilt-wing/thrust.jpg)|![contour](tilt-wing/contour.jpg)|
_Obtained results through computational simulation_

* Entire UAV geometry was assembled with all the componenets such as wings, fuselage and propellers to perform simulations using moving reference frames for the propellers using [Ansys].

| | | |
|-|-|-|
|![fullUAVCM](tilt-wing/fullUAVCM.jpg)|![forward](tilt-wing/forward.jpg)|![vertical](tilt-wing/vertical.jpg)|
_Results obtained from computational simulations of the UAV_


* With the estimated control inputs, altiude controller was modelled using [MATLAB Simulink]

| | | |
|-|-|-|
|![motorcontrol](tilt-wing/motorcontrol.jpg)|![motorcontrol1](tilt-wing/motorcontrol1.jpg)|![altitudecontrol](tilt-wing/altitudecontrol.jpg)|
_vertical motor model_                _forward motor model_                           _altitude controller_

* Control inputs such as thrust coefficient and rotor mass moment of inertia, response of the controller was recorded for step input

  ![response](tilt-wing/response.jpg)
  _Step reseponse_


*  `Attitude controller` for the UAV is under development.

---


[experiment datasheet]: https://store.tmotor.com/product/v505-vtol-motor.html
[MATLAB Simulink]: https://in.mathworks.com/products/simulink.html
[CATIA]: https://www.3ds.com/products/catia/catia-v5
[Ansys]: https://www.ansys.com/en-in
