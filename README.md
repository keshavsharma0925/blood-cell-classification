# Blood Cell Classification

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/keshavsharma0925/blood-cell-classification/blob/main/blood_cell_classification.ipynb)

A deep learning project developed for **APS360: Applied Fundamentals of Deep Learning** at the University of Toronto. The project explores automated classification of microscopic white blood cell images using artificial and convolutional neural networks.

## Project Overview

The goal of this project was to classify white blood cell images into four categories:

- Eosinophils
- Lymphocytes
- Monocytes
- Neutrophils

A baseline artificial neural network (ANN) was first developed and compared against a custom convolutional neural network (CNN) designed for image classification.

## Dataset

The project used a blood cell image dataset containing four approximately balanced white blood cell classes.

After data cleaning:

- **12,513 total images**
- **2 duplicate images removed**
- **0 unreadable images**

### Class Distribution

| Class | Images |
|---|---:|
| Eosinophil | 3,131 |
| Lymphocyte | 3,109 |
| Monocyte | 3,102 |
| Neutrophil | 3,171 |

A stratified split was used to maintain similar class distributions across the datasets:

- **Training:** 8,759 images
- **Validation:** 1,877 images
- **Testing:** 1,877 images

Images were resized to **64 × 64 RGB** and preprocessing and augmentation techniques were applied before model training.

## Model Development

### Baseline ANN

A fully connected artificial neural network was developed as a baseline for comparison.

**Validation Results:**

- Validation Accuracy: **25.4%**
- Macro F1 Score: **0.103**
- Validation Loss: **1.386**
- Trainable Parameters: **1,573,508**

The baseline model performed close to random classification and heavily favoured the neutrophil class, demonstrating the limitations of a fully connected network for this image classification task.

### Custom CNN

A custom convolutional neural network was developed to better capture spatial features within the blood cell images.

The architecture included:

- 3 convolutional layers
- 16, 32, and 64 feature channels
- ReLU activation functions
- 2 × 2 max-pooling
- 128-unit fully connected layer
- Dropout regularization
- 4-class output layer

**Validation Results:**

- Best Validation Accuracy: **90.1%**
- Final Validation Accuracy: **89.5%**
- Macro F1 Score: **0.895**
- Validation Loss: **0.234**
- Trainable Parameters: **548,516**

The CNN achieved substantially higher classification performance while using fewer trainable parameters than the baseline ANN.

## Test Results

The final CNN achieved approximately **90% test accuracy** with a **0.90 macro F1 score**.

| Class | Precision | Recall | F1 Score |
|---|---:|---:|---:|
| Eosinophil | 0.88 | 0.77 | 0.82 |
| Lymphocyte | 0.97 | 0.98 | 0.97 |
| Monocyte | 0.95 | 0.98 | 0.97 |
| Neutrophil | 0.81 | 0.87 | 0.84 |

The model performed particularly well on **lymphocytes and monocytes**, while most remaining classification errors occurred between **eosinophils and neutrophils**.

## Model Comparison

| Model | Validation Accuracy | Macro F1 | Validation Loss | Parameters |
|---|---:|---:|---:|---:|
| Baseline ANN | 25.4% | 0.103 | 1.386 | 1,573,508 |
| Custom CNN | 89.5% | 0.894 | 0.234 | 548,516 |

The custom CNN improved validation accuracy by approximately **64 percentage points** while using substantially fewer trainable parameters.

## Technologies Used

- Python
- PyTorch
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Google Colab

## Skills Demonstrated

- Deep Learning
- Convolutional Neural Networks
- Image Classification
- Data Cleaning and Preprocessing
- Stratified Dataset Splitting
- Data Augmentation
- Model Training and Validation
- Performance Evaluation
- Confusion Matrix Analysis
- Hyperparameter Tuning
- Python Programming

## Notebook

The complete project notebook, including data preprocessing, model development, training, validation, and testing, is available here:

**[`blood_cell_classification.ipynb`](./blood_cell_classification.ipynb)**

You can also use the **Open in Colab** button at the top of this page to explore the notebook directly.

## Author

**Keshav Sharma**  
Chemical Engineering, University of Toronto

[LinkedIn](https://www.linkedin.com/in/keshavv-sharma)
