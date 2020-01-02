# Distracted-Driver-Detection 

## Overview:
Driving a car is a complex task, and it requires complete attention. Distracted driving is any activity that takes away the driver’s attention from the road. The National Highway Traffic Safety Administration (NHTSA) reported that 36,750 people died in motor vehicle crashes in 2018, and 12% of it was due to distracted driving. 

Many States now have laws against texting, talking on a cell phone, and other distractions while driving. We believe that computer vision can augment the efforts by the governments to prevent accidents caused by distracted driving. Our algorithm automatically detects the distracted activity of the drivers and alerts them. We envision this type of product being embedded in cars to help drivers avoid distraction.

We took the StateFarm dataset which contains snapshots from a video captured by a camera mounted in the car. Training set has ~22.4 K samples with equal distribution among the classes and 79.7 K unlabeled test samples. There are 10 classes of images:

There are 10 classes including safe driving in the dataset:
- c0	Safe driving.
- c1	Texting (right hand).
- c2	Talking on the phone (right hand).
- c3	Texting (left hand).
- c4	Talking on the phone (left hand).
- c5	Operating the radio.
- c6	Drinking.
- c7	Reaching behind.
- c8	Hair and makeup.
- c9	Talking to passenger(s).

This dataset is available on Kaggle, under the State Farm competition:
https://www.kaggle.com/c/state-farm-distracted-driver-detection


In order to predict the class, we started with VGG-16 and trained it on extra layers. We then tuned the parameters, trained it on all layers and used different models - RESNET50, XCEPTION and MOBILE NET models. The models were then ensembled to predict the images. To further improving the ensembling method we used KNN smoothing. Since the images are all snapped from video snippets there were substantial number of images from the same class that were similar. Based on this premise, we found similar images and averaged the probabilities over these images which helped us smoothen predicted probabilities for each class. 



Following is the general proess followed while running different models : 

- Image Augmentation by rotating it and then shifting the width and height of the image. Then only a specific region of the image was     taken to further improve the accuracy of the image 
- Splitting the data into train, validation and test 
- Running Models by training extra layer first and then all layers 
- Optimizing parameters : number of epochs, batchses and optimizer
- Running differnt models and repeating the process 
- Ensembling the few selected models 

The log loss we achieved is in top 12 percentile on Kaggle

## The Team:
Amey Athaley, Apoorva Jasti, Jayant Raisinghani, Sadhana Koneni and Satya Naren Pachigolla from The University of Texas at Austin. For the complete review of the project-work, please find our blog post - https://towardsdatascience.com/distracted-driver-detection-using-deep-learning-e893715e02a4



