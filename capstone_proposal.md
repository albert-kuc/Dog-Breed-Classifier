# Machine Learning Engineer Nanodegree
## Capstone Proposal
Albert Kuc  
03/11/2020

## Dog Breed Classifier

### Domain Background

As a self taught learner I'm exploring ML and DL fields for some time now, although I have not yet defined a clear 
preference and narrowed my field of interest. An app proposal to classify dogs detected in images is a step forward for 
myself to gain basic experience of what could lead me towards computer vision.

This project is one of the standard projects at Udacity's Nanodegrees programs both for ML and DL. At first it may seem 
simple, as we may believe to be ready to tackle bigger world problems straight away, but when think about it in more 
depth, it offers a number of challenges, especially to less experienced students. It explores areas such as image 
processing, object detection as well as training a neural network, which in my opinion always offers more fun than 
simpler ML models, when there is a reason to apply it.   

### Problem Statement

The goal of this project is to build an app foundations to classify dogs. This model may be later used to develop a web 
or mobile app. It accepts an image as input and feedback a breed of all dogs found in it. An app can be then used to 
help user define a dog's breed just by uploading it's photo. Furthermore this app also offers a humor aspect. If any 
uploaded image contain humans it will classify them as well, to determine a resembling dog breed.

### Datasets and Inputs

The datasets used in this project are provided by Udacity. First is the dogImages dataset which contains 133 sets of dog 
images categorised by breed. The images are already split into train, test and validate folders with number of 6680, 
836, 835 images respectively. Second is the lfw dataset which contains over 13k images of humans. \
During the pre-processing images will be converted to grayscale and resized. Additionally data augmentation to increase 
the number of images will be taken into consideration.  

### Solution Statement

The final solution for this project be capable to determine whether there is a dog or a human in an image. If it finds a
dog, it will return corresponding breed. In case there is a human in the image instead, it will return resembling dog 
breed. This solution will be a model build on the principle of Convolution Neural Network. CNN is a Deep Learning 
algorithm used specifically when working with images. 

### Benchmark Model

As the benchmark model we will use a basic CNN build from scratch. The aim for this model is to predict dog breed with 
an accuracy of at least 10%. 

A second benchmark model will be a pre-trained model. A pre-trained model is a model that was trained on a large 
benchmark dataset to solve a problem similar to the one that we want to solve (e.g. VGG, Inception, ResNet). This model 
is expected to achieve an accuracy of minimum 60%. 

### Evaluation Metrics

To evaluate the model we will rely on accuracy which is a common metric for classification tasks. It will be calculated
by dividing the number of correct classified images by the total number of images used. 

### Project Design

This final section will provide a brief description of the workflow algorithm. The following steps will be used in order
to solve the given task:

1. Import datasets \
In this section two sets of images will be loaded. Both will be analyzed in terms of usefulness for the project.

2. Detect human faces \
For the purpose of detecting human faces we will use Haar feature-based cascade classifier. This is one of OpenCV's 
pre-trained detectors. A common requirement to use this kind of detectors is to convert images to grayscale. If the 
number of objects detected in the image is above 0 then the image contains a human face.

3. Detect dogs \
Here we will use VGG-16, a pre-trained PyTorch model. This model has been trained on ImageNet, a very large and very
popular dataset, used for image classification and other vision tasks. Given an image the pre-trained VGG-16 model 
returns a prediction from the 1000 possible categories. Output in range 151-268 corresponds to specific dog breeds. 

4. Classify dog breed \
As mentioned above for the purpose of predicting dog breed we will create a Convolution Neural Network. The goal of this
model would be to outperform the benchmark models with the accuracy metric. 

5. Final model \
The final model would take and image as input. If that image contains a dog it would return it's breed. If it contains a
human it would return resembling dog breed. Otherwise, if neither would return a message that indicates error.
