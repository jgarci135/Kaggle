# Kaggle Competition
# Deep Learning with Python, Keras & Tensorflow

In this work there is a basic workthrough of using an keras API written in Python to work with the Kaggle Dog Breed Classification compeition. This file also has a way to connect to google drive which at the time of making this file there was no readily easy way for Google Colab to interact or pull information from Google drive.  Using Google drive was much more reliable then adding any large files to the colab with the chance to lose them

# The Object of the Dog Breed Competition
The point of the compeition was to take dogs and identify them and classify them within 120 differing categories.


As a contextual reference, deep learning is a subset of machine learning that allows algorithms to train itself in order to perform tasks like image and speech recognition. Deep learning accomplishes this by revealing immense amounts of data to multi-layered neural networks.

This document will walk you through the entire process of:

Setting up Google Drive to mount a virtual drive
Load the dog images from Kaggle
Transform the images for use by Keras and CNNs
Make test and training groups
Prepare data to fit into a deep learning model
Use a Functional API deep learning model
with inception module architecture
Use BatchNormalization to decrease overfitting
Create submission file to Kaggle for evaluation
