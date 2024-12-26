# Plant disease detection and remedy using ResNet and Pandas Dictionary
## Overview
We developed a neural network to detect plant diseases and provide necessary remedy. 

## Problem Statement
Plant diseases cause approximately <b> $220 billion in annual losses globally </b> as per the US Department of Agriculture. Therefore, detecting and curing plant diseases is crucial for boosting agricultural production and ensure financial wellbeing of farmers. 

## Methods
<b> 1. Data Preparation: </b> Redistibuted data among train, validation and test directories to resolve data imbalance issues detected. Resized and normalized images to ensure standardization. 

<b> 2. Modeling: </b> The Convolutional Neural Network (CNN) consisted of four convolutional layers, each paired with batch normalization and ReLU activation for stability and improved convergence. MaxPooling layers were integrated to reduce spatial dimensions, and residual connections were added to overcome vanishing gradient issues. 

<b> 3. Training: </b> Trained on PyTorch for 8 epochs using Cross Entropy loss function. 
Hyperparameters: Batch size= 64 | Number of epochs = 8 | Max learning rate = 0.005 | Gradient clip = 0.15 | Weight decay = 1e-4 | Optimizer function = SGD

<b> 4. Remedy Mapping: Pandas dictionary was created connecting each disease to possible remedy suggested by US Department of Agriculture.  

## Results 
The model achieved a test accuracy of 99.4% in detecting disease and was able to provide the fetch the relevant remedy from the pandas dictionary. However, it struggled to predict similar looking diseases (e.g. predicting potato early blight as pepper bacterial spot as both have similar looking leaves and cause pale spots).  

## Recommendations
Expanding the dataset to include more plant species, including more diverse images for diseases and leaves that look similar.

