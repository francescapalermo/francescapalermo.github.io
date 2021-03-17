---
title: "Tactile and proximity dataset"
collection: datasets
type: "Dataset"
permalink: /dataset/tactileproximitydataset
excerpt: 'Tactile and proximity sensing can be efficiently used to perform automatic crack detection. 
This dataset was acquired with a fibre optic based finger-shaped sensor which slided on a total of 10 different 3D printed surfaces for a total of 50 acquistions.
The acquired data can be used for fracture detection on surfaces using both tactile and proximity features.
'
venue: ""
location: ""
---

Tactile and proximity sensing can be efficiently used to perform automatic crack detection. 
This dataset was acquired with a fibre optic based finger-shaped sensor which slided on a total of 10 different 3D printed surfaces.
The acquired data can be used for fracture detection on surfaces using both tactile and proximity features.


###Acquisition Protocol:
A set of 10 objects with different surfaces (no crack, cracks of different widths, a bump and a wavy pattern) and crack widths (0mm, 1mm, 2mm, 5mm, 8mm, 10mm)  were manufactured with 
PLA plastic using 3D printing technology (Ultimaker~III, 0.2 mm layer height, 0.4 mm nozzle diameter). 
The wavy pattern consists of a repeated pattern of sine waves of 1mm amplitude and 5mm magnitude.
The Phantom Omni moved the tactile sensor across the sample objects: the periodic sliding has a  magnitude of 1.6 cm and a frequency of 1000 Hz. 
The average sliding velocity was 3.89 mm/s. 
The initial position of the tactile sensors was not controlled and varied from trial to trial and was set at approximately 5-10 mm from the crack edge.
No normal force was applied by the sensor to the sampled surfaces except the force caused by the sensor weight (approx 200 g).
Tactile and proximity signals were recorded for 12 repeated continuous sliding movements. 
This continuous recording was repeated five times.


###Acquisition Setup: 
To collect data and test the proposed crack detection algorithm, 
the tactile and proximity sensor has been attached to the end-effector of a Touch desktop haptic interface (formerly known as Phantom Omni Geomagic)). 
The Phantom Omni was programmed to slide the tactile sensor along a static sample surface following a programmed periodic movement. 
Data from tactile and proximity sensors were recorded through an Arduino Mega ADK micro-controller, connected via a USB port, at 400 Hz. 
These data were later synchronised with the absolute position of the tip of the tactile sensor calculated through the encoder readings of the Phantom Omni.
Data acquisition and control were implemented through dedicated software libraries (OpenHaptics and Robotic Operating System) running on an Ubuntu desktop computer.
The material samples, as well as the Phantom Omni interface, were fixed to a laboratory desk to minimise any vibration and unwanted displacements.


The complete setup and implemented analysis is throughly described in the following [paper](https://www.frontiersin.org/articles/10.3389/frobt.2020.513004/full)


###Information
The names are encoded as follows:<br/>
"crack_type/width_R.mat"<br/>
type/width: the type of surface or the width of the crack<br/>
R: the number of complete repetition <br/>

For each surface the dataset contains one matlab file:
TBD


###Download links
TBD


###Info and queries
For any enquiries, questions, concerns and general feedback, please contact f.palermo@qmul.ac.uk.


###Acknowledgments
If you use the dataset, please cite the paper.
Bibtext Citation: 

`@article{palermo2020automatic, title={Automatic Fracture Characterization Using Tactile and Proximity Optical Sensing}, author={Palermo, Francesca and Konstantinova, Jelizaveta and Althoefer, Kaspar and Poslad, Stefan and Farkhatdinov, Ildar}, journal={Frontiers in Robotics and AI}, volume={7}, year={2020}, publisher={Frontiers Media SA}}`

