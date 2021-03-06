# Dog-Breed Classifier
This is the second project of the Udacity Deep Learning Nanodegree Program.  

## Setting up the virtual environment

1. >pip install virtualenv
2. >python -m venv env
3. > cd .\env\Scripts
4. >activate
5. >pip install -r requirements.txt
6. >python -m ipykernel install --name=\<choose-a-name-to-be-displayed-in-jupyter\>

## Problem statement
We want to build a deep **c**onvolutional **n**eural **n**etwork (CNN) that can detect the breed when it's given an image of a dog. When it's provided with an image of a human face, the algorithm shall identify the resembling dog breed :P

## Solution
A human face detector is built using OpenCV's [Cascade Classifier](https://docs.opencv.org/master/db/d28/tutorial_cascade_classifier.html). A dog detector is built via transer learning, using the pre-trained [VGG16](https://neurohive.io/en/popular-networks/vgg16/) model. In order to classify dog breeds, a deep CNN is built from scratch - consisting of four convolutional and three fully connected layers. Batch normalization is applied after each convolutional layer to avoid covariance shift and accelerate the training process. Furthermore, max pooling layers are added to decrease the number of features and avoid overfitting. The latter is also supported by adding dropout layers. ReLU is consistently used as the activation function.  
The modelling is mainly performed with the PyTorch library.  

Exemplary images and outputs:  
* Dog:  
![Example Image 1](/example2.png)
* Human:  
![Example Image 2](/example1.png)

  