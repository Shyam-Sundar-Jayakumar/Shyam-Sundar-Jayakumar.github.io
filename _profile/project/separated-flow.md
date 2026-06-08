Understanding the dominant coherent structures governing separated turbulent boundary layer flows through modal decomposition techniques and reconstruction frameworks based on backflow dynamics.

_Representative reconstruction and modal analysis_

| | | |
|-|-|-|
|![spod](backflow/spod.jpg)|![reconstruction](backflow/reconstruction.jpg)|![backflow](backflow/backflow.jpg)|

        _SPOD modes_              _Flow reconstruction_             _Backflow field_

---

##### Goal of this project

* To study the dominant coherent structures present in separated turbulent boundary layers.
* To implement modal decomposition techniques such as POD, DMD and SPOD.
* To develop reduced-order reconstruction frameworks based on backflow dynamics.
* To evaluate the accuracy of the reconstructed flow fields.

---

##### Motivation

Separated turbulent boundary layers contain a wide range of flow structures interacting across multiple length and time scales. Understanding these structures using reduced-order techniques can provide valuable physical insight while significantly reducing the complexity of the dataset.

This project focuses on investigating whether backflow dynamics can be used to reconstruct and understand separated flow behavior.

---

##### Research process

_Preparation of velocity datasets_

* Time-resolved velocity fields were processed and decomposed into mean and fluctuating components.
* The datasets were prepared for modal decomposition and statistical analysis.

| | |
|-|-|
|![instantaneous](backflow/instantaneous.jpg)|![meanflow](backflow/meanflow.jpg)|

          _Instantaneous velocity field_           _Mean velocity field_

---

_Implementation of modal decomposition techniques_

* POD, DMD and SPOD were implemented to identify dominant flow structures.
* Modal energies and frequency content of the structures were analyzed.

| | | |
|-|-|-|
|![pod](backflow/pod.jpg)|![dmd](backflow/dmd.jpg)|![spodmode](backflow/spodmode.jpg)|

          _POD mode_                 _DMD mode_                  _SPOD mode_

---

_Development of reconstruction framework_

* Reduced-order reconstructions were generated using selected modal coefficients.
* The reconstructed flow fields were compared with the original datasets.

| | |
|-|-|
|![original](backflow/original.jpg)|![reconstructed](backflow/reconstructed.jpg)|

          _Original flow field_            _Reconstructed flow field_

---

_Analysis of backflow dynamics_

* Backflow regions were identified throughout the dataset.
* Correlations between backflow and dominant modal structures were investigated.

![backflowcorr](backflow/backflowcorr.jpg)

_Analysis of backflow dynamics_

---

##### Current status

* POD, DMD and SPOD frameworks have been successfully implemented.
* Reconstruction methodologies are currently being evaluated.
* Analysis of backflow-based reconstruction performance is ongoing.

---
