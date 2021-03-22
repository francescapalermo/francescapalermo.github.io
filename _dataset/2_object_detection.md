---
title: "Annotated fracture dataset for object detection"
collection: datasets
type: "Dataset"
permalink: /dataset/objectdetection
excerpt: 'Localising and recognising the presence of mechanical fractures is an important task necessary in hazardous environments during waste decommissioning.
It is especially useful to avoid spillage from containers keeping chemical and radioactive waste or to identify concrete fractures at early stages, 
to prevent their growth which may lead to larger macro-scale catastrophic failures.
This dataset consists of 3000 labelled images of fractures and 24000 labelled augmented images.
The acquired data can be used for fracture localisation with object detection.
'
venue: ""
location: ""
---

Localising and recognising the presence of mechanical fractures is an important task necessary in hazardous environments during waste decommissioning.
It is especially useful to avoid spillage from containers keeping chemical and radioactive waste or to identify concrete fractures at early stages, 
to prevent their growth which may lead to larger macro-scale catastrophic failures.
This dataset consists of 3000 labelled images of fractures and 24000 labelled augmented images.
The acquired data can be used for fracture localisation with object detection.


### Information
This dataset consists of a subset of manually labelled 3000 RGB images with 227x227 size, representing fractures in concrete extracted from the unlabeled [openly-available dataset](https://data.mendeley.com/datasets/5y9wdsg2zt/2). 
The images were captured approximately 1m away from the surfaces with the camera facing directly to the target. 
The images were acquired on the same day with similar illumination conditions. 
No data augmentation in terms of random rotation or flipping is applied. 

Each image was annotated for object detection purpose.
All the images were manually labelled with [LabelImg](https://github.com/tzutalin/labelImg), a graphical image annotation tool.


### Augmentation Steps
The images available in the implemented dataset were similar to each other and did not have any occlusions or other objects beside the crack. 
This is not optimal when training an object detection model. 
Thus, multiple data augmentation processes were implemented to make the model more robust.
First, all the images (one or two at a time) were randomly pasted in a randomly chosen bigger background figure.
In addition, at each turn, the script could randomly generate and paste in the same background a patch with no crack to avoid having 
the model basing the detection only on the grey patches and not the fractures themselves.
Then, to create occlusions to the crack, to each of the resulting and original images, a random number of different screws (between 1 and 2) was added to random positions.
Finally, a random set of data augmentation was applied.
The complete set of augmentations consists of changing the HSV (hue, saturation, lightness), horizontal flip, scale, translate, rotate and shear.
For each image, the script decided on a random set of the previously described augmentation and applied that to augment the image.
The labels of the original dataset were adopted accordingly to the various modifications during the augmentation process.
After the augmentation steps, a total of (approx.) 24000 images were created.


Example of images used for the crack localisation and detection.
<ol type="a">
<li> Original images of the dataset; </li>
<li> Original images added to various backgrounds. A random number of cracks and nocrack is included; </li>
<li> A various number of screws added to the previous figures to create occlusion; </li>
<li> Data augmentation applied to all the previous figures. </li>
</ol>

![augmentation Image](https://github.com/francescapalermo/francescapalermo.github.io/blob/master/_dataset/set_cracks.png?raw=true)

### Download links
[Original](https://github.com/francescapalermo/francescapalermo.github.io/blob/master/_dataset/object_detection/base_images.rar?raw=true) dataset.


[Augmented](https://www.dropbox.com/s/20a15u8zz1jf047/augmented.rar?dl=0?raw=true) dataset.


### Info and queries
For any enquiries, questions, concerns and general feedback, please contact [Francesca Palermo](mailto:f.palermo@qmul.ac.uk)


### Acknowledgments
If you use the dataset, please cite the following [paper](https://www.frontiersin.org/articles/10.3389/frobt.2020.513004/full).
Bibtext Citation: 

`@article{palermo2020automatic, title={Automatic Fracture Characterization Using Tactile and Proximity Optical Sensing}, author={Palermo, Francesca and Konstantinova, Jelizaveta and Althoefer, Kaspar and Poslad, Stefan and Farkhatdinov, Ildar}, journal={Frontiers in Robotics and AI}, volume={7}, year={2020}, publisher={Frontiers Media SA}}`

