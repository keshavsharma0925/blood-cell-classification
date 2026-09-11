# Blood Cell Classification

A deep learning project developed for APS360 at the University of Toronto to classify microscopic white blood cell images into four classes:

- Eosinophils
- Lymphocytes
- Monocytes
- Neutrophils

## Project Overview

The goal of this project was to explore the use of deep learning for automated blood cell classification. The project compared a baseline artificial neural network with a convolutional neural network designed for image classification.

## Dataset

The project used the Kaggle Blood Cell Images dataset.

- 12,515 original images
- 12,513 images after removing duplicates
- 70% training
- 15% validation
- 15% testing
- Images resized to 64 × 64 RGB

## Model

The primary model was a custom convolutional neural network built in PyTorch.

Architecture:
- 3 convolutional layers with 16, 32, and 64 filters
- ReLU activation
- 2 × 2 max pooling
- 128-unit fully connected layer
- Dropout of 0.3
- 4-class output layer

## Technologies

- Python
- PyTorch
- NumPy
- Matplotlib
- Google Colab

## Key Features

- Image preprocessing and normalization
- Data augmentation using flips and rotations
- Baseline ANN comparison
- CNN training and evaluation
- Classification performance analysis
