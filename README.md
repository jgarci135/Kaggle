# Kaggle Competition
# Deep Learning with Python, Keras & Tensorflow

In this work there is a basic work through of using an keras API written in Python to work with the Kaggle Dog Breed Classification competition. This file also has a way to connect to google drive which at the time of making this file there was no readily easy way for Google Colab to interact or pull information from Google drive.  Using Google drive was much more reliable then adding any large files to the colab with the chance to lose them

## The Object of the Dog Breed Competition
The point of the competition was to take dogs and identify them and classify them within 120 differing categories.

This document will walk you through the entire process of:
- Setting up Google Drive to mount a virtual drive.

- Load the dog images from Kaggle.

- Transform the images for use by Keras and CNNs.

- Make test and training groups.

- Prepare data to fit into a deep learning model.

- Use a Functional API deep learning model with inception module architecture.
- Use BatchNormalization to decrease overfitting.

- Create submission file to Kaggle for evaluation.

The Code can be found in the file **Dog_Classification_NAME.ipynb.**  
## Explanations of methods and models

## Results Summary
The results of the score uploaded to Kaggle are placed at 5.03557 which places the results of the project in the bottom half of the public leaders as they were submitted.  
The biggest difference to most of the leaders on the board are the use of transferred learning or resource allocation.  This preparation of the data was created without the use of and transferred rates from either the Stanford data sets or the larger sets for images that included dogs.  
Without using the additional test sets or using augmentation of the Dog breed images there is not enough data to increase the learning of features to better the results. The best rates using the inception model with four layers and reducing the picture quality and size to be used in the model while running multiple epochs and saving the weights for each run and the purposed hyper parameters are limited to about 25% accuracy of the validation set.
## Issues and pitfalls
Resources to run this type of data set must be significant enough to help with the ease of finding the best possible results.  GoogleColab is a free service and will allocate about 12-13 mb of RAM for the virtual machine and has a 12 hour limit of continuous use.  
First issue is that Google Colab is not integrated with any directories which require a work around to get files into Colab.  Its possible to load directly to CoLab but if a disconnect occurs the file must be re-uploaded.  This is an issue for files that are >500mb file as they can take upwards of 1 hour to upload.  The solution to this is to upload them once to Google Drive and then us a mounted drive inside of Google Colab to pull the information to work on.  This is much faster.  An issue to this is that the Colab is slow as cycling through the mounted drive and loops which make pre-processing difficult on Google Colab.  It was necessary to use the local drive to pre-processes all the images and then create the numpy arrays and upload them to Google Drive and then use them in the Colab.  The Colab was being used mainly for the GPU computational power.  
It was necessary to also change the file size from 256x256 which kept the image resolution near picture quality to 128x128 which degraded the image quality and possibly the ability for the model to find important features.  
