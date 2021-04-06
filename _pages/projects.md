---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
redirect_from:
  - /projects
---
# Table of Contents
- [Fracture Characterisation and Geometry for Motion Planning](#fracture-characterisation-and-geometry-for-motion-planning)
- [Fracture Detection and Localisation](#fracture-detection-and-localisation)
- [Bilateral Teleoperation Franka Panda/Geomagic Touch](#bilateral-teleoperation-franka-panda-geomagic-touch)
- [Hololyo](#hololyo)
- [Nao Interface](#nao-interface)
- [EEG Classification and Analysis](#eeg-classification-and-analysis)
- [Motion Reconfiguration for Kuka Manipulator via Visual Servoing](#motion-reconfiguration-for-kuka-manipulator-via-visual-servoing)
- [The Little Knight](#the-little-knight)



Fracture Characterisation and Geometry for Motion Planning
---------------
Previously, a multi-modal system for fracture detection and localisation in extreme environments (e.g., nuclear power plant) was developed using vision techniques (e.g., object
detection) to localise possible fractures. These coordinates are explored by a fibre optic sensor, attached as an end-effector to a manipulator, to confirm the presence of the fracture
via online classification methods of the tactile and proximity data.

The crack's image can be further analysed to extract the geometry information and to plan an optimal control tactile exploration.
To analyse the obtained localised crack images, image processing and computer vision techniques are implemented to create a skeletonised version of the image of the fracture
which is then transformed into a graph. 

First, the acquired image of the fracture is converted to grey scale colours and then blurred with a Gaussian filter (3x3 kernel).
The resulting image is converted to a binary image using a combination of Otsu and binary thresholds.
Once the binary image is obtained, morphological transformations are applied to it. 
Dilation is applied to join possible broken parts of the image of the crack.
Then, Canny Edge detection is implemented. 
The average of the intensities of the pixels is used to automatically construct the lower and higher threshold for edge detection.
The resulting edges are improved with additional morphological transformations (dilation).
Using the obtained edges, the contours of the fractures are calculated.
Calculation of the median surface area of the contours is used to eliminate the outliers (to remove the contours areas which are much smaller than the median).
The mask of the object is then created, which is later implemented to design a skeletonised version of the fracture.
The pruned skeleton, to avoid small fragments, is then used to build the graph of the fracture.
For brevity, the original image, the mask, the pruned skeleton and the graph are shown below.

![graph Image](https://github.com/francescapalermo/francescapalermo.github.io/blob/master/_projects/graph.png?raw=true)

Middle points of the edges of the previously preliminary graph are extracted and an updated graph made up of these middle points is created. Each of this middle point is connected to
the rest of the points via Euclidean distance. The distance is used to create the weighted edges of the graph. Knowing these coordinates and weights will be useful for the tactile
sensors motion planning as it will be possible to define the required tactile exploration path.
Graph theory is then applied to investigate the possible exploration path. Since the goal of the experiment is to explore all the possible nodes with the smallest cost, a revised version of
the Minimum Spanning Tree is implemented. Each node of the graph is explored only once and the minimum path from the starting node is found.
For each node, left and right position are included. These will later be used for the exploration of the fracture with the robotic manipulator.

<img src="https://github.com/francescapalermo/francescapalermo.github.io/blob/master/_projects/crack_graph.gif" width="300" height="200" />
![Alt Text](https://github.com/francescapalermo/francescapalermo.github.io/blob/master/_projects/crack_graph.gif)



Fracture Detection and Localisation
---------------	
Developed an innovative approach involving vision and tactile sensing to detect and characterise surface cracks. 
The proposed algorithm localises surface cracks in a remote environment through videos/photos taken by an on-board robot camera, which is then followed by automatic tactile inspection of the surfaces. 
Faster R-CNN deep learning-based **object detection** is used for identifying the location of potential cracks. 
**Random forest classifier** is used for tactile identification of the cracks to confirm their presences. 
The algorithm is able to localise and explore fractures both offline and in realtime.
When using both modalities cooperatively, the model is able to correctly detect 92.85% of the cracks while it decreases to 46.66% when using only vision information. 
Exploring a surface using only tactile requires around 199 seconds. This time is reduced to 31 seconds when using both vision and tactile together. 
This approach may be implemented also in extreme environments (e.g. in nuclear plants) since gamma radiation does not interfere with the basic sensing mechanism of fibre optic-based sensors.


\[[VIDEO](https://www.youtube.com/embed/dbRd6R_bzNE)\]

For more information, check the related papers \[[1](https://www.frontiersin.org/articles/10.3389/frobt.2020.513004/full)\], \[[2](https://ieeexplore.ieee.org/abstract/document/9196936)\]


[![Watch the video](https://github.com/francescapalermo/francescapalermo.github.io/blob/master/_projects/multi_modal_algorithm_horizontal_complete.png?raw=true)](https://www.youtube.com/embed/dbRd6R_bzNE)


Bilateral Teleoperation Franka Panda/Geomagic Touch
---------------
Developed the master side in C++ of a bilateral teleoperation system between Geomagic Touch as the master device and a Franka Emika’s Panda as the slave robot.
The system consists of a hybrid position and rate control modes with interoperability protocol.


\[[VIDEO](https://www.youtube.com/embed/QcAdntJHpo8)\]

For more information, check the related paper \[[PDF](https://link.springer.com/chapter/10.1007/978-3-030-23807-0_26)\]


[![Watch the video](https://github.com/francescapalermo/francescapalermo.github.io/blob/master/_projects/positioncontrol.jpg?raw=true)](https://www.youtube.com/embed/QcAdntJHpo8)



Hololyo
---------------	
Portable **augmented reality** application to provide visual feedback to amputees during surface electromyography data acquisitions.
Developed in Unity to combines the **Microsoft HoloLens** and the **Thalmic labs Myo**. 
In the augmented environment, rendered by the HoloLens, the user can control a virtual hand with surface electromyography. 
By using the virtual hand, the user can move objects in augmented reality and train to activate the right muscles for each movement through visual feedback.

For more information, check the related paper \[[PDF](https://link.springer.com/chapter/10.1007/978-3-030-25332-5_1)\]

![hololyo Image](https://github.com/francescapalermo/francescapalermo.github.io/blob/master/_projects/hololyo.png?raw=true)



Nao Interface
---------------	
Mobile application for **Android** which allows the user to send vocal commands to a
Nao Robot, through a client-server connection. 

The project is created with two different applications which collaborates with each other:
1. An Android app which sends vocal human commands in real-time to a Choreographe project;
2. A Coreographe interface which transmits the the received message to the NAO robot.

The NAO is able to recognize a set of words in any sentence and executes multiple commands at the same time.


\[[CODE](https://sites.google.com/view/nao-interface)\] \[[VIDEO](https://www.youtube.com/embed/1wWJvQwiVUg)\]

[![Watch the video](https://github.com/francescapalermo/francescapalermo.github.io/blob/master/_projects/nao.png?raw=true)](https://www.youtube.com/embed/1wWJvQwiVUg)


EEG Classification and Analysis
---------------	
Analysis and classification of a [EEG signals datatbase](http://archive.ics.uci.edu/ml/datasets/EEG+Database) through the usage of the software [Neucube](https://kedri.aut.ac.nz/R-and-D-Systems/neucube).

**NeuCube** is a software development environment for **spiking neural network** (SNN) prototype systems. 
It facilitates the design and the implementation of efficient solutions to problems through precise selection and testing of most suitable methods and parameters 
for a Spatio-Temporal Data Machine (STDM).

The goal of the implemented database is to analyse EEG correlations of genetic predisposition to alcoholism. 
It contains measurements from 64 electrodes placed on subject's scalps which were sampled at 256 Hz (3.9-msec epoch) for 1 second.
The database consisted in two classes of subjects: alcoholic and control. 
Each subject was exposed to either a single stimulus (S1) or to two stimuli (S1 and S2) which were pictures of objects. 
When two stimuli were shown, they were presented in either a matched condition where S1 was identical to S2 or in a non-matched condition where S1 differed from S2.
In total, data were acquired from 122 subjects and each subject completed 120 trials where different stimuli were shown. 
The electrode positions were located at standard sites, following Standard Electrode Position Nomenclature

\[[PRESENTATION](https://github.com/francescapalermo/francescapalermo.github.io/blob/master/_projects/neucube.pdf)\]



Motion Reconfiguration for Kuka Manipulator via Visual Servoing
---------------	
Medical Robotics project for controlling the pose of a **Kuka manipulator** via Mutual-Information Based on Visual Servoing.
Visual Servoing uses the information acquired by a vision sensors (such as cameras) for feedback control of the pose/motion of a robot.
The proposed method can be used in medical applications for multimodal alignment, e.g. to compare multiple CT scans to monitor cancer mass growth.

Project developed with **Matlab** and **OpenCV**.

\[[PRESENTATION](https://github.com/francescapalermo/francescapalermo.github.io/blob/master/_projects/visual_servoing.pdf)\]


The Little Knight
---------------	
The project is based on **WebGL** library that provides a graphic 3D API to browsers, allowing the creation of 3D scenes through **Javascript**, working with the Canvas element of HTML5.
Two additional libraries are implemented:
* **Three.js**, open source library based on WebGL, that provides a number of functions and structures that simplify the creation of complex objects and scenes, altogether leaving the programmer free to personalize the scene at his own.
* **Physi.js** (website), another open source library that handles Physic simulation through Three.js function.

The project developed is a third person game in which the player impersonates a character named Knight.
The goal of the game is to reach the dragon on the other side of the cave, avoiding the lava’s river.
In case of victory, the game stops and a final victory screen will appear.
Otherwise, if the character falls in the lava, the losing screen will appear.

\[[PRESENTATION](https://github.com/francescapalermo/francescapalermo.github.io/blob/master/_projects/littleKnight.pdf)\]

![littleknight Image](https://github.com/francescapalermo/francescapalermo.github.io/blob/master/_projects/littleknight.png?raw=true)
