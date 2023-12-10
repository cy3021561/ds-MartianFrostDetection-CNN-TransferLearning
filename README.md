# Martian HiRISE Image Classification Project

## Overview

This project aims to build a classifier to identify frost in Martian terrain images, leveraging a dataset created to study Mars’ seasonal frost cycle. The focus is on applying convolutional neural networks (CNN) and transfer learning techniques.

## Dataset

- **Source**: [NASA's JPL Dataverse - Martian HiRISE Images](https://dataverse.jpl.nasa.gov/dataset.xhtml?persistentId=doi:10.48577/jpl.QJ9PYA)
- **Content**: The dataset contains 214 subframes and a total of 119920 tiles, labeled as 'frost' or 'background.'

## Part 1: Data Exploration and Pre-processing

### (a) Data Organization

- Images are organized into 299x299 tiles, derived from 5120x5120 pixel subframes of HiRISE images.
- Tiles are classified into two categories: 'background' and 'frost.'

### (b) Data Splits

- The dataset includes predefined splits for training, testing, and validation sets.

## Part 2: Training CNN + MLP

### (a) Image Augmentation

- Perform image augmentation techniques like cropping, zooming, rotating, flipping, adjusting contrast, and translation.

### (b) CNN Model Training

- Train a three-layer CNN followed by a dense layer (MLP).
- Implement ReLU activation, softmax function, batch normalization, 30% dropout rate, L2 regularization, and ADAM optimizer.
- Train for at least 20 epochs with early stopping based on validation set performance.

### (c) Evaluation

- Report Precision, Recall, and F1 score for the CNN + MLP model.
- Plot the training and validation errors vs. epochs.

## Part 3: Transfer Learning

### (a) Pre-trained Models

- Utilize pre-trained models like EfficientNetB0, ResNet50, and VGG16.
- Train only the last fully connected layer, freezing the earlier layers.

### (b) Empirical Regularization and Training

- Apply similar image augmentation techniques as in CNN training.
- Use ReLU activation in the last layer, softmax, batch normalization, 30% dropout, and ADAM optimizer.
- Train for 10 to 20 epochs with early stopping.

### (c) Evaluation

- Report Precision, Recall, and F1 score for each transfer learning model.
- Plot the training and validation errors vs. epochs.

### (d) Comparison and Analysis

- Compare the results of the CNN + MLP model with the transfer learning models.
- Discuss the outcomes and insights gained.

## Objectives

- To develop a robust classifier for identifying frost in Martian HiRISE images.
- To compare the effectiveness of CNN + MLP models with transfer learning approaches using pre-trained networks.
- To evaluate the models based on precision, recall, and F1 score, and understand the impact of image augmentation and transfer learning on classification performance.
