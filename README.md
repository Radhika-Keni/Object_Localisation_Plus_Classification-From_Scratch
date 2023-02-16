# Object_Localisation_Plus_Classification-From_Scratch
Build a model that does localization and classification(from scratch) on the Oxford IIT Data set



## Objective of this notebook
- The purpose of this notebook is to build a model that performs object classification and localisation in one network
- Details of the **problem statement**  , **data set** ,  **summary of the code/solution**  , **sample output/Prediction** from the program and **final result** of the project are listed in the sections to follow.

## Problem Statement 
Build a model to that performs object classification and localisation


## Data Description:
 - Data Set :Oxford IIT Pet Data 
 - Link : https://www.robots.ox.ac.uk/~vgg/data/pets/


## Summary of the Solution/Code:
The code aims at building a simple bounding  box to detect the animal's face 
- We begin by building a utility class to to read the input images ,convert them to a structured format for further processing and model building and pickle the created input data files Code @ **Read_& Structure_Input.ipynb**
- We then do an EDA on the data and  check various statistics on the images such as total no of images , whether classes are balanced and display a few images with their bounding boxes for visulaization . Code @ **EDA.ipynb**
- We will then we will pre-process the input data to make it compatible for model building wherein we first do a Train-Test split and create 2 subsets (70:30 split), convert all images to tensors for both subsets,resize all the images to one pre-defined size, convert bounding boxes accordingly,convert classification labels to one hot vectors ,visualize data and see that everything looks good. Code @ **Pre-Processing_Data.ipynb**
- We then build the model which is a keras image classifier with a base network of mobile net(pre-trained on image Net) and add a regression head and a  classification head to it
- Finally we train the model , log the results and run an inference. Code @ **Train_And_Inference.ipynb**



## Sample Ouput/Prediction :
Here is a sample Ouput image from  the program/model 

![image](https://user-images.githubusercontent.com/68383273/219475048-55f185c0-b419-4ab8-a528-9a4b60f409fa.png)



## Result
- We built a model capable of doing object localisition + object classification in a single network
- The scores of the model as displayed in the logs were accuracy= 0.9955  and IoU = 0.9452 on the validation/testing data set

## References & Guidance
- PGP GL/UAT study material 
- https://learnopencv.com/classification-with-localization/


