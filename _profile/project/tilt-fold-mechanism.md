An Unmanned Aerial Vehicle configuration integrated with tilting mechanism of the rotors for forward flight for efficiency, and wing folding mechanism for the wings for compact storage


_Design of the mechanism_

| | |
|-|-|
|![isotiltfold](tilt-wing/isotiltfold.jpg)|![sidetiltfold](tilt-wing/sidetiltfold.jpg)|
                      _Conceptual CAD model_ 

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

The following methodology is used to design and fabricate the tilting and folding m

_CAD model of the gear mechanism_

* Initially, conceptual design of the mechanism was generated using [CATIA] and the gears required for the mechanism was modelled.

| | |
|-|-|
|![mechaiso](tilt-wing/mechaiso.jpg)||![tiltiso](tilt-wing/tiltiso.jpg)|
     _Conceptual CAD model of the gear setup for folding and tilting mechanism_ 

_Estimation of gear design parameters_

* To form a proper gear assembly, the design parameters of the gears were estimated and with the exact dimensions their geometry was prepared

| | |
|-|-|
|![gearparameters](tilt-wing/gearparameters.jpg)|![drafttilt](tilt-wing/drafttilt.jpg)|
          _Parameters to consider estimation_             _Drafting of the modelled assembly_   

* With the estimated dimensions of the gear, the process proceeded for the production of the parts.

|![3dprint](tilt-wing/3dprint.jpg)|
  _3-D printed gears for the assembly_


* With the prepared models, the gears were assembled to produce the exact model as the conceptual design

| | |
|-|-|
|![foldmech](tilt-wing/foldmech.jpg)|![tiltmech](tilt-wing/tiltmech.jpg)|
          _Folding mechanism_                       _Tilting mechanism_ 

* Moving forward, these mechanism were integrated with the necessary components such as servo motors and rotors for the test model
  ![completemech](tilt-wing/completemech.jpg)
  _Test assembly of the mechanism integrated with all the necessary components to form the configuration of the UAV_


*  `Fabrication of the UAV` is not much focused on this test model, but it is in progress for future works.

---


[experiment datasheet]: https://store.tmotor.com/product/v505-vtol-motor.html
[MATLAB Simulink]: https://in.mathworks.com/products/simulink.html
[CATIA]: https://www.3ds.com/products/catia/catia-v5
[Ansys]: https://www.ansys.com/en-in
