#Semantc Segmentation Project

## Introduction
We construct a fully convoutional neural network based on the VGG-16 image classifier to perform semantic segmentation to identify drivable area of the road from a car's dash camera image.


### Architecture

A VGG-16 network (pre-trained) is converted to a fully convolutional network by converting the final FCL to a 1x1 convolution and setting the depth equal to 2 ( Number of classes in this case. Road and not road). Skip connections are used to improve performance. 1x1 convoutions are performed on previous VGG ayers ie layers 3 and 4 and adding them elementwise to upsampled lower-level layers.

### Optimizer

Cross entropy and Adam optimizer is used as the loss function

### Hyper parameters

-batch size : 5
-learning_rate : 5
- epochs : 50
- learning_rate: 0.0009


##Result

The loss function after 50 epochs was in the range of 0.03
The network is able to classify roads vs non road pretty well.
But it is not perfect

## Image samples

![sample_images](./umm_00042.png)
![sample_images](./umm_00040.png)
![sample_images](./umm_00012.png)
![sample_images](./umm_00070.png)

