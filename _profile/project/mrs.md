Prediction of drag forces on non-spherical particles in low Reynolds number flows through the implementation of a three-dimensional Method of Regularized Stokeslets (MRS) solver.

_Validation of the MRS solver for spheres and ellipsoids_

| | | |
|-|-|-|
|![sphere](regularized-stokeslets/figure2a.png)|![ellipsoid](regularized-stokeslets/figure2b.png)|![ellipsoid45](regularized-stokeslets/figure2c.png)|

_Sphere streamline visualization_          _Ellipsoid streamline visualization_          _Ellipsoid at 45° orientation_

---

##### Goal of this project

* To develop a three-dimensional Method of Regularized Stokeslets solver for drag prediction.
* To investigate the influence of particle geometry on drag characteristics.
* To validate numerical predictions against analytical solutions for spheres and ellipsoids.
* To study the variation of drag force with particle aspect ratio and orientation.
* To extend the methodology to non-uniform flow conditions.

---

##### Motivation

Prediction of drag forces on non-spherical particles is important in multiphase flows, aerosol transport, sediment transport and biological systems. While analytical solutions exist for simple geometries, accurate prediction of drag on arbitrary particle shapes remains challenging.

This project focuses on implementing the Method of Regularized Stokeslets to efficiently predict drag forces on spheres and ellipsoids under low Reynolds number flow conditions.

---

##### Research process

_Development of the Method of Regularized Stokeslets solver_

* A three-dimensional Method of Regularized Stokeslets solver was developed in MATLAB.
* The particle surface was discretized into boundary nodes and quadrature weights.
* The resulting linear system was solved to obtain surface tractions and drag forces.

---

_Validation against analytical solutions_

* Drag predictions were computed for spheres and ellipsoids with aspect ratios ranging from highly oblate to highly prolate geometries.
* Numerical predictions were compared against analytical drag formulations available in literature.

![validation](regularized-stokeslets/figure1.png)

_Drag variation with aspect ratio and comparison with analytical solutions_

---

_Investigation of particle orientation effects_

* Simulations were performed for multiple particle orientations relative to the incoming flow.
* The influence of angle of attack on drag force was investigated.

| | |
|-|-|
|![aoa_mrs](regularized-stokeslets/figure3a.png)|![aoa_dns](regularized-stokeslets/figure3b.png)|

_Drag variation with angle of attack using MRS_          _Comparison with DNS data from literature_

---

##### Results

* Successfully developed a three-dimensional Method of Regularized Stokeslets solver in MATLAB.
* Achieved an average drag prediction error of approximately 1.8% compared with analytical solutions.
* Accurately captured drag trends across a wide range of particle aspect ratios.
* Demonstrated agreement with published DNS data for varying particle orientations.
* Extended the methodology to non-uniform flow environments with prediction errors below 2%.

---

##### Software and tools

* MATLAB
* Method of Regularized Stokeslets
* GMRES Solver
* Numerical Linear Algebra
* Low Reynolds Number Hydrodynamics

---
