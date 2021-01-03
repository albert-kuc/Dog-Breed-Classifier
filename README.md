## Dog Breed Classifier

This repository contains my capstone project "Dog Breed Classification" for 
[Machine Learing Engineer Nanodegree](https://www.udacity.com/course/machine-learning-engineer-nanodegree--nd009t) 
program
at Udacity.

### Problem Statement
The goal of this project is to build foundations for an app to classify dogs. 
This model may be later used to develop a web or mobile app. \
It accepts an image as input and returns a breed for a dog found in it. 
The application can be used to help user define a dog's breed just by uploading it's photo. \
Furthermore this app also offers a humor aspect. 
If any uploaded image contain humans instead, it will classify the person as well to determine a resembling dog breed.

### Required libraries and versions

| Library | Version |
| ------ | ------ |
| Python | 3.6.9 |
| NumPy | 1.19.4 |
| tqdn | 4.41.1 |
| cv2 | 4.1.2 |
| matplotlib | 3.2.2 |
| torch | 1.7.0 |
| torchvision | 0.8.1 |
| PIL | 7.0.0 |

### Instructions

The original Udacity project instructions can be found [here](https://github.com/udacity/deep-learning-v2-pytorch/tree/master/project-dog-classification).

Direct links to access the datasets used in the project:
* Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip). Unzip the folder and place it in this project's home directory, at the location /dogImages.
* Download the [human dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip). Unzip the folder and place it in the home diretcory, at location /lfw.