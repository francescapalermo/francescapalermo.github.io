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


<img src="https://github.com/francescapalermo/francescapalermo.github.io/blob/master/_projects/multi_modal_algorithm_horizontal_complete.png?raw=true"/>


<iframe width="320" height="240"
src="https://www.youtube.com/embed/UEqlDOTNtKc">
</iframe>

For more information, check the related papers [1](https://www.frontiersin.org/articles/10.3389/frobt.2020.513004/full), [2](https://ieeexplore.ieee.org/abstract/document/9196936)

Hololyo
======
Portable augmented reality application to provide visual feedback to amputees during surface electromyography data acquisitions.
Developed in Unity to combines the Microsoft HoloLens and the Thalmic labs Myo. 
In the augmented environment, rendered by the HoloLens, the user can control a virtual hand with surface electromyography. 
By using the virtual hand, the user can move objects in augmented reality and train to activate the right muscles for each movement through visual feedback.



Nao Interface
======
Mobile application for Android which allows the user to send vocal commands to a
Nao Robot, through a client-server connection. 

The project is created with two different applications which collaborates with each other:
1. An Android app which sends vocal human commands in real-time to a Choreographe project;
2. A Coreographe interface which transmits the the received message to the NAO robot.

The NAO is able to recognize a set of words in any sentence and executes multiple commands at the same time.


Available [here](https://sites.google.com/view/nao-interface)

[![Watch the video](https://github.com/francescapalermo/francescapalermo.github.io/blob/master/_projects/nao.png)](https://www.youtube.com/embed/1wWJvQwiVUg)



EEG Classification and Analysis
======
Classification of EEG signals through the usage of the software Neucube


OpenCV-Matlab Kuka Control
======
Medical Robotics project based on interaction between Matlab and OpenCV based on paper Mutual-
Information Based on Visual Servoing (A. Dame, E. Marchand)

The Little Knight
======
Game based on WebGL using Javascript library (Three.js).