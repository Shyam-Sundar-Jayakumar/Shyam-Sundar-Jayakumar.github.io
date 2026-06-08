Understanding the dominant coherent structures governing separated turbulent boundary layer flows through modal decomposition and reconstruction techniques based on backflow dynamics.

_Representative flow reconstruction and modal analysis_

| | | |
|-|-|-|
|![meanflow](backflow/meanflow.jpg)|![spod](backflow/spod.jpg)|![reconstruction](backflow/reconstruction.jpg)|

_Mean flow field_      _SPOD mode structure_      _Flow reconstruction_

---

##### Goal of this project

* To investigate the dominant coherent structures present in separated turbulent boundary layers.
* To implement modal decomposition techniques such as POD, DMD and SPOD.
* To develop reconstruction frameworks using reduced modal representations.
* To study the relationship between backflow dynamics and separated flow behavior.
* To quantify reconstruction accuracy using statistical error metrics.

---

##### Motivation

Separated turbulent boundary layers are commonly encountered in aerospace applications and are associated with increased drag and flow instability. While modal decomposition techniques can identify dominant coherent structures, the ability of localized backflow information to reconstruct global flow behavior remains an open research question.

This project focuses on understanding whether backflow can be used as a physically meaningful indicator to reconstruct separated turbulent flow fields using reduced-order representations.

---

##### Research process

_data preparation_

* Time-resolved velocity datasets were processed and decomposed into mean and fluctuating components.
* Spatial and temporal consistency checks were performed before modal analysis.

| | |
|-|-|
|![instantaneous](backflow/instantaneous.jpg)|![mean](backflow/mean.jpg)|

_Instantaneous velocity field_          _Mean velocity field_

---

_modal decomposition_

* Proper Orthogonal Decomposition (POD), Dynamic Mode Decomposition (DMD) and Spectral Proper Orthogonal Decomposition (SPOD) were implemented.
* Dominant coherent structures and their associated modal energies were extracted.

| | | |
|-|-|-|
|![pod](backflow/pod.jpg)|![dmd](backflow/dmd.jpg)|![spod](backflow/spodmode.jpg)|

_POD modes_      _DMD modes_      _SPOD modes_

---

_flow reconstruction_

* Reduced-order reconstructions were generated using selected modal coefficients.
* Multiple modal combinations were tested to determine the minimum modal content required for accurate reconstruction.

| | |
|-|-|
|![orig](backflow/original.jpg)|![recon](backflow/reconstructed.jpg)|

_Original field_        _Reconstructed field_

---

_error analysis_

* Reconstruction quality was evaluated using RMSE, correlation coefficients and energy recovery metrics.
* Performance comparisons were conducted across POD, DMD and SPOD methodologies.

![error](backflow/error.jpg)

_Reconstruction error distribution_

---

##### Results

* Successfully implemented POD, DMD and SPOD frameworks.
* Demonstrated accurate reconstruction using a reduced set of dominant modes.
* Identified relationships between backflow dynamics and coherent flow structures.
* Established a framework for physics-based reconstruction of separated turbulent flows.

---
