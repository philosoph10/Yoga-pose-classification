# Yoga Pose Classification using Computer Vision

![Yoga Pose](https://c.ndtvimg.com//yoga_625x300_1529482160763.jpg)

## Overview

This repository contains a Jupyter notebook for a Kaggle competition focused on yoga pose classification. Yoga has gained immense popularity over the years, especially in the wake of the COVID-19 pandemic, as people seek ways to maintain their physical and mental well-being from the comfort of their homes. Correctly performing yoga poses is essential, as each pose targets specific muscle groups, and practicing them incorrectly can be unproductive or even harmful.

The competition addresses the challenge of human pose estimation for yoga, which involves complex body postures. Existing computer vision methods may struggle with asanas involving horizontal body postures or complex poses. In this competition, the task is formulated as a classification problem, where participants are required to classify different yoga asanas into six classes, aiming for higher Mean F1 scores as the evaluation metric.

## Solution

### Data Preparation

The solution starts by organizing the dataset for training and validation using the provided CSV file, ensuring that each class maintains its representation in both categories. The key steps include copying and splitting the data into respective folders.

### Model Architecture

The core of the solution is a Convolutional Neural Network (CNN) for image classification. The model is based on the RegNetX040 architecture, with an added Global Average Pooling layer and a dense output layer for the six yoga pose classes. The model is pretrained on ImageNet, which helps in extracting relevant features from yoga pose images.

### Training

The model is trained with a multi-stage approach, starting with a higher learning rate and gradually reducing it in subsequent stages. The training process involves data augmentation, which includes random rotation, horizontal and vertical shifts, shear transformations, zoom, and horizontal flip. This helps the model generalize better and achieve higher accuracy.

### Model Evaluation

The model's performance is evaluated using the validation set, and the best model is saved based on validation accuracy. This saved model is then used to make predictions on the test dataset.

## Results

The solution achieved a Mean F1 score of 0.89 on the Kaggle competition. The code provided in this notebook demonstrates the complete pipeline from data preparation to model training and evaluation. You can use this code as a starting point to tackle similar computer vision problems or yoga pose classification tasks.

For more details, refer to the [Jupyter Notebook](yoga-pose-classification.ipynb) in this repository.
