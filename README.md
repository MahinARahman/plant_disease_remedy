# Plant disease detection and remedy using ResNet and Pandas Dictionary
## Overview
We developed a neural network (ResNet-9) to detect plant diseases and provide necessary remedy. 

## Problem Statement
Plant diseases cause approximately <b> $220 billion in annual losses globally </b> as per the US Department of Agriculture. Therefore, detecting and curing plant diseases is crucial for boosting agricultural production and ensuring financial wellbeing of farmers. 

## Methods
<b> 1. Data Preparation: </b> Redistibuted data among train, validation and test directories to resolve data imbalance issues detected. Resized and normalized images to ensure standardization. 

<b> 2. Modeling: </b> The Convolutional Neural Network (CNN) consisted of four convolutional layers, each paired with batch normalization and ReLU activation for stability and improved convergence. MaxPooling layers were integrated to reduce spatial dimensions, and residual connections were added to overcome vanishing gradient issues. 

<b> 3. Training: </b> Trained on PyTorch for 8 epochs using Cross Entropy loss function. 
Hyperparameters: Batch size= 64 | Number of epochs = 8 | Max learning rate = 0.005 | Gradient clip = 0.15 | Weight decay = 1e-4 | Optimizer function = SGD

<b> 4. Remedy Mapping </b>: Pandas dictionary was created connecting each disease to possible remedy suggested by US Department of Agriculture.  

## Results 
The model achieved a test accuracy of 99.4% in detecting plant diseases and was able to fetch the relevant remedy from the pandas dictionary. However, it struggled to predict similar looking diseases (e.g. predicting potato early blight as pepper bell bacterial spot as both plants have similar looking leaves and the diseases share symptoms like discolored spots).  

## Recommendations
Expanding the dataset to include more plant species, including more diverse images for diseases and leaves that look similar.

## Data Source
New Plant Diseases Dataset: https://www.kaggle.com/datasets/vipoooool/new-plant-diseases-dataset/data?select=New+Plant+Diseases+Dataset%28Augmented%29

## Files
**1. Project_Plant_friend (1).ipynb**: Jupyter Notebook for data preparation, model training and evaluation with visualizations.

**2. Project Plant Friends Report (1).pdf**: Report detailing the methodology, analysis, insights and way forward.

**3. Plant_disease_remedies.csv**: csv file including list of diseases and their possible remedies suggested by US Department of Agriculture.  

**4. README.md**: Project documentation.

## Setup
Clone the repository: git clone https://github.com/MahinARahman/plant_disease_remedy.git

Upload provided csv file consisting of disease remedies. 




