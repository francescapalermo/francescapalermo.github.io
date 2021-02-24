---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---



Fracture Detection and Localisation
======
Developed an innovative approach involving vision and tactile sensing to detect and characterise surface cracks. 
The proposed algorithm localises surface cracks in a remote environment through videos/photos taken by an on-board robot camera, which is then followed by automatic tactile inspection of the surfaces. 
Faster R-CNN deep learning-based object detection is used for identifying the location of potential cracks. 
Random forest classifier is used for tactile identification of the cracks to confirm their presences. 
The algorithm is able to localise and explore fractures both offline and in realtime.
When using both modalities cooperatively, the model is able to correctly detect 92.85% of the cracks while it decreases to 46.66% when using only vision information. 
Exploring a surface using only tactile requires around 199 seconds. This time is reduced to 31 seconds when using both vision and tactile together. 
This approach may be implemented also in extreme environments (e.g. in nuclear plants) since gamma radiation does not interfere with the basic sensing mechanism of fibre optic-based sensors.


[VIDEO](https://www.youtube.com/embed/UEqlDOTNtKc)

[![Watch the video](https://github.com/francescapalermo/francescapalermo.github.io/blob/master/_projects/multi_modal_algorithm_horizontal_complete.png?raw=true)](https://www.youtube.com/embed/UEqlDOTNtKc)


For more information, check the related papers [1](https://www.frontiersin.org/articles/10.3389/frobt.2020.513004/full), [2](https://ieeexplore.ieee.org/abstract/document/9196936)

Hololyo
======
Portable augmented reality application to provide visual feedback to amputees during surface electromyography data acquisitions.
Developed in Unity to combines the Microsoft HoloLens and the Thalmic labs Myo. 
In the augmented environment, rendered by the HoloLens, the user can control a virtual hand with surface electromyography. 
By using the virtual hand, the user can move objects in augmented reality and train to activate the right muscles for each movement through visual feedback.



Nao Interface
======
Mobile application for **Android** which allows the user to send vocal commands to a
Nao Robot, through a client-server connection. 

The project is created with two different applications which collaborates with each other:
1. An Android app which sends vocal human commands in real-time to a Choreographe project;
2. A Coreographe interface which transmits the the received message to the NAO robot.

The NAO is able to recognize a set of words in any sentence and executes multiple commands at the same time.


[CODE](https://sites.google.com/view/nao-interface) [VIDEO](https://www.youtube.com/embed/1wWJvQwiVUg)

[![Watch the video](https://github.com/francescapalermo/francescapalermo.github.io/blob/master/_projects/nao.png?raw=true)](https://www.youtube.com/embed/1wWJvQwiVUg)


EEG Classification and Analysis
======
Analysis and classification of a [EEG signals datatbase](http://archive.ics.uci.edu/ml/datasets/EEG+Database) through the usage of the software [Neucube](https://kedri.aut.ac.nz/R-and-D-Systems/neucube).

NeuCube is a software development environment for spiking neural network (SNN) prototype systems. 
It facilitates the design and the implementation of efficient solutions to problems through precise selection and testing of most suitable methods and parameters 
for a Spatio-Temporal Data Machine (STDM).

The goal of the implemented database is to examine EEG correlations of genetic predisposition to alcoholism. 
It contains measurements from 64 electrodes placed on subject's scalps which were sampled at 256 Hz (3.9-msec epoch) for 1 second.
The database consisted in two classes of subjects: alcoholic and control. 
Each subject was exposed to either a single stimulus (S1) or to two stimuli (S1 and S2) which were pictures of objects. 
When two stimuli were shown, they were presented in either a matched condition where S1 was identical to S2 or in a non-matched condition where S1 differed from S2.
In total, data were acquired from 122 subjects and each subject completed 120 trials where different stimuli were shown. 
The electrode positions were located at standard sites, following Standard Electrode Position Nomenclature
[Presentation](https://github.com/francescapalermo/francescapalermo.github.io/blob/master/_projects/neucube.pdf)



Motion Reconfiguration for Kuka Manipulator via Visual Servoing
======
Medical Robotics project for controlling the pose of a Kuka manipulator via Mutual-Information Based on Visual Servoing.
Visual Servoing uses the information acquired by a vision sensors (such as cameras) for feedback control of the pose/motion of a robot.
The proposed method can be used in medical applications for multimodal alignment, e.g. to compare multiple CT scans to monitor cancer mass growth.
<br>Project developed with Matlab and OpenCV.</br>
[Presentation](https://github.com/francescapalermo/francescapalermo.github.io/blob/master/_projects/visual_servoing.pdf)


The Little Knight
======
The project is based on **WebGL** library that provides a graphic 3D API to browsers, allowing the creation of 3D scenes through **Javascript**, working with the Canvas element of HTML5.
Two additional libraries are implemented:
* **Three.js**, open source library based on WebGL, that provides a number of functions and structures that simplify the creation of complex objects and scenes, altogether leaving the programmer free to personalize the scene at his own.
* **Physi.js** (website), another open source library that handles Physic simulation through Three.js function.

The project developed is a third person game in which the player impersonates a character named Knight.
The goal of the game is to reach the dragon on the other side of the cave, avoiding the lava’s river.
In case of victory, the game stops and a final victory screen will appear.
Otherwise, if the character falls in the lava, the losing screen will appear.
[Presentation](https://github.com/francescapalermo/francescapalermo.github.io/blob/master/_projects/littleKnight.pdf)

![littleknight Image](https://github.com/francescapalermo/francescapalermo.github.io/blob/master/_projects/littleknight.png?raw=true)
