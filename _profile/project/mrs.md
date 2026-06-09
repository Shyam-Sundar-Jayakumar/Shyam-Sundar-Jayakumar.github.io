Prediction of drag forces on non-spherical particles in low Reynolds number flows through the implementation of a three-dimensional Method of Regularized Stokeslets (MRS) solver.

_Validation of the MRS solver for spheres and ellipsoids_

| | | |
|-|-|-|
|![sphere](regularized-stokeslets/sphere.jpg)|![ellipsoid](regularized-stokeslets/ellipsoid.jpg)|![validation](regularized-stokeslets/validation.jpg)|

_Sphere streamline visualization_          _Ellipsoid flow field_          _Drag validation against analytical solutions_

---

##### Goal of this project

* To develop a three-dimensional Method of Regularized Stokeslets solver for drag prediction.
* To investigate the influence of particle geometry on drag characteristics.
* To validate numerical predictions against analytical solutions for spheres and ellipsoids.
* To study the variation of drag with particle aspect ratio and angle of attack.
* To extend the methodology to non-uniform flow conditions.

---

##### Motivation

Prediction of drag forces on non-spherical particles plays an important role in multiphase flows, sediment transport, aerosol dynamics, and biological systems. While analytical solutions exist for simple geometries, predicting drag on arbitrary particle shapes remains challenging.

This project focuses on implementing the Method of Regularized Stokeslets to develop an efficient framework for predicting drag on spheres and ellipsoids under low Reynolds number flow conditions.

---

##### Research process

_Surface discretization of particle geometries_

* Spherical and ellipsoidal geometries were generated using a Fibonacci-based surface discretization method.
* Multiple aspect ratios ranging from highly prolate to highly oblate particles were considered.

| | |
|-|-|
|![spheremesh](regularized-stokeslets/spheremesh.jpg)|![ellipsoidmesh](regularized-stokeslets/ellipsoidmesh.jpg)|

_Surface discretization of sphere_          _Surface discretization of ellipsoid_

---

_Implementation of the Method of Regularized Stokeslets_

* A three-dimensional Method of Regularized Stokeslets solver was developed using MATLAB.
* The particle surface was discretized into boundary nodes with associated quadrature weights.
* The resulting dense linear system was solved using the GMRES iterative solver.

| | |
|-|-|
|![matrix](regularized-stokeslets/matrix.jpg)|![solver](regularized-stokeslets/solver.jpg)|

_Formation of the linear system_          _Numerical solution procedure_

---

_Validation against analytical solutions_

* Drag predictions for spheres were compared against the classical Stokes drag formulation.
* Ellipsoid drag predictions were validated against analytical solutions for both prolate and oblate spheroids.
* The influence of aspect ratio on drag force was investigated.

| | |
|-|-|
|![dragcomparison](regularized-stokeslets/dragcomparison.jpg)|![error](regularized-stokeslets/error.jpg)|

_Comparison of analytical and numerical drag_          _Prediction error analysis_

---

_Analysis of particle orientation effects_

* Simulations were performed for multiple particle orientations relative to the incoming flow.
* The variation of drag force with angle of attack was analyzed and compared with literature results.

| | |
|-|-|
|![aoa](regularized-stokeslets/aoa.jpg)|![aoavalidation](regularized-stokeslets/aoavalidation.jpg)|

_Drag variation with angle of attack_          _Comparison with literature data_

---

_Application to non-uniform flows_

* The solver was extended to linear shear and parabolic flow profiles.
* Numerical predictions were validated using Faxén law corrections.

| | |
|-|-|
|![shear](regularized-stokeslets/shear.jpg)|![parabolic](regularized-stokeslets/parabolic.jpg)|

_Linear shear flow_          _Parabolic flow_

---

##### Results

* Successfully developed a three-dimensional Method of Regularized Stokeslets solver.
* Achieved an average drag prediction error of approximately 1.8% compared to analytical solutions.
* Accurately captured drag trends across particle aspect ratios ranging from 0.1 ≤ b/a ≤ 10.
* Demonstrated agreement with published drag trends for varying particle orientations.
* Extended the methodology to non-uniform flow environments with prediction errors below 2%.

---

##### Software and tools

* MATLAB
* Method of Regularized Stokeslets
* GMRES Solver
* Numerical Linear Algebra
* Low Reynolds Number Hydrodynamics

---
