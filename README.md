# Melanoma Skin Cancer Detection

## Problem Statement:
To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution which can evaluate images and alert the dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

## Table of Contents
* [General Info](#general-information)
* [Data Reading/Data Understanding](#data-reading/data-understanding)
* [Data Visualization](#data-visualization)
* [Data Augmentation](#data-augmentation)
* [Model Building/Training](#model-building)
* [Conclusion](#conclusion)


## General Information
- We are required to build a CNN model without using any pretrained model using transfer learning to detect melanoma skin cancer from an image. The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.
The data set contains the following diseases:
   1) Actinic keratosis
   2) Basal cell carcinoma
   3) Dermatofibroma
   4) Melanoma
   5) Nevus
   6) Pigmented benign keratosis
   7) Seborrheic keratosis
   8) Squamous cell carcinoma
   9) Vascular lesion

## Data Reading/Data Understanding
- Created train & validation dataset from the train directory (which have subdirectories for each category) with a batch size of 32 and resized all images to (180,180,3) shape.

## Data Visualization
- Visualized one instance of all the nine categories present in the training dataset using matplotlib.

## Data Augmentation
- Applied data augmentation using keras.layers and added it to CNN model architecture along with dropout to reduce overfitting.
- Used Augmentor external package as well for handling class balance purpose which will add new generated images to train_directory file.

## Model Building
- Built a CNN model using Sequential model which includes data_augmentation, data_rescaling (between [0,1]), convolutional layers, Max Pooling layers, Dropout , Flatten and FC layers which detect 9 classes of an image.

## Conclusion
- Training with augmented images using Augmentor is highly desirable as it is giving very good accuracy on training and validation both datasets with maintaining class balance.
- To avoid chances of overfitting, we have to add data_augmentation and dropout in CNN model architecture.

## Contact
Created by [@chintan4560] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
