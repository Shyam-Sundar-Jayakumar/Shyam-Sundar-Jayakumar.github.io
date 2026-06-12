Modal Reconstruction of Separated Turbulent Boundary Layer Flows using POD, SPOD and Backflow-Based Evaluation.

_Investigation of separated-flow reconstruction using modal decomposition techniques_

| | | |
|-|-|-|
|![setup](modal-analysis/figure1.jpg)|![spod_modes](modal-analysis/figure5r.png)|![reconstruction](modal-analysis/figure7.png)|

_Experimental setup_          _Leading SPOD modes_          _Flow reconstruction comparison_

---

##### Goal of this project

* To investigate separated turbulent boundary layer dynamics using modal decomposition techniques.
* To implement Proper Orthogonal Decomposition (POD) and Spectral Proper Orthogonal Decomposition (SPOD).
* To reconstruct separated-flow velocity fields using reduced-order representations.
* To evaluate reconstruction quality using backflow percentage as a physics-based metric.
* To compare energy-ranked and frequency-resolved reconstruction frameworks.

---

##### Motivation

Separated turbulent boundary layers are commonly encountered in aerodynamic systems and contain complex interactions between coherent structures, broadband turbulence, and intermittent backflow events.

This project investigates whether reduced-order modal representations can accurately reconstruct physically meaningful separation dynamics and whether backflow can be used as a robust metric to evaluate reconstruction performance.

---

##### Research process

_Experimental dataset and flow configuration_

* Time-resolved PIV measurements of separated turbulent boundary layers over ramp and bump geometries were analyzed.
* Both geometries produce adverse-pressure-gradient-induced separation and backflow dynamics.

![setup_large](modal-analysis/figure1.jpg)

_Experimental ramp and bump configurations_

---

_Identification of coherent structures using SPOD_

* Spectral Proper Orthogonal Decomposition was implemented to identify coherent structures organized by frequency.
* Low-frequency structures associated with separated shear-layer motion were investigated.

|![bump_modes](modal-analysis/figure5b.png)|![ramp_modes](modal-analysis/figure5r.png)|

_Leading SPOD modes for the bump and ramp datasets_

---

_SPOD spectral analysis_

* Frequency-resolved energy spectra were computed to identify dominant energetic frequencies in the separated flow.
* Low-frequency peaks were associated with large-scale separation dynamics.

| | |
|-|-|
|![bump_spectrum](modal-analysis/figure6b.png)|![ramp_spectrum](modal-analysis/figure6r.png)|

_SPOD energy spectra_

---

_Modal reconstruction of separated flows_

* POD and SPOD reconstructions were generated using reduced modal representations.
* Reconstructed velocity fields were compared with the original PIV data.

![reconstruction](modal-analysis/figure7.png)

_top left original data, top right: POD reconstruction, bottom left: SPOD reconstruction, bottom right: DMD reconstruction_    

* Reconstructed velocity fields were distinct according to their modal decomposition. However visual interpretation cannot give a qualititative analysis on evauluating the methods

---

_Backflow reconstruction analysis_

* Global backflow percentage was used as a physics-based metric to evaluate reconstruction quality.
* POD, SPOD and DMD predictions were compared with the original measurements.

| | |
|-|-|
|![bump_timeseries](modal-analysis/figure8b.png)|![ramp_timeseries](modal-analysis/figure8r.png)|

_Global Backflow for bump geometry_          _Global Backflow for ramp geometry_


---

_Spatial reconstruction assessment_

* Wall-normal backflow profiles were evaluated at multiple streamwise locations.
* Reconstruction accuracy was assessed throughout the separated-flow region.

| | |
|-|-|
|![bump_profiles](modal-analysis/figure9.png)|![ramp_profiles](modal-analysis/figure10.png)|

_Backflow profiles for bump geometry_          _Backflow profiles for ramp geometry_

---

_Quantitative error analysis_

* Root Mean Square Error (RMSE) was computed to compare reconstruction performance.
* POD and SPOD were evaluated across multiple streamwise locations.


|![bump_rmse](modal-analysis/figure11b.png)|![ramp_rmse](modal-analysis/figure11r.png)|

_Backflow profiles RMSE for bump_          _Backflow profiles RMSE for ramp_

---

##### Results

* Successfully implemented POD and SPOD frameworks for separated turbulent boundary layer datasets.
* Developed a backflow-based framework for evaluating modal reconstructions.
* POD reconstruction with 100 retained modes produced lower backflow RMSE than SPOD for both ramp and bump geometries. :contentReference[oaicite:7]{index=7}
* SPOD provided improved physical interpretation through frequency-resolved coherent structures. :contentReference[oaicite:8]{index=8}
* Demonstrated that reproducing backflow dynamics is significantly more challenging than reproducing visually similar velocity contours. :contentReference[oaicite:9]{index=9}

---

##### Software and tools

* MATLAB
* Proper Orthogonal Decomposition (POD)
* Spectral Proper Orthogonal Decomposition (SPOD)
* Dynamic Mode Decomposition (DMD)
* Particle Image Velocimetry (PIV)
* Reduced-Order Modeling
* Turbulent Boundary Layer Analysis

---
