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
