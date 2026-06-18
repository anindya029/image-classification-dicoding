# Image Classification using CNN

## Project Overview
This repository contains a deep learning project aimed at detecting and classifying stages of Alzheimer's Disease from brain MRI images. The model is built using a custom Convolutional Neural Network (CNN) architecture with TensorFlow/Keras and is designed to run in a Google Colab environment.

## Dataset
The dataset used in this project is the Augmented Alzheimer MRI Dataset, available on Kaggle.

Dataset source:

https://www.kaggle.com/datasets/uraninjo/augmented-alzheimer-mri-dataset

The data consists of MRI images. The data has four classes of images both in training as well as a testing set:

- Mild Demented
- Moderate Demented
- Non Demented
- Very Mild Demented

The data contains two folders. One of them is augmented ones and the other one is originals.
Originals could be used for validation or test dataset…

Data is augmented from an existing dataset. Original images can be seen in Data Explorer.
https://www.kaggle.com/datasets/tourist55/alzheimers-dataset-4-class-of-images

## Project Overview
This project includes:
1. Data Preparation
2. Data Preprocessing
3. Model Training
4. Model Export

## Model Architecture
The model is a Sequential Convolutional Neural Network structured to prevent overfitting while capturing fine spatial features:

- Convolutional Layers: 4 Conv2D layers with progressive filter sizes (32, 64, 64, 128), utilizing ReLU activation.

- Pooling Layers: MaxPooling2D layers following each convolution block to reduce spatial dimensions.

- Regularization: Integrated Dropout layers (0.2 after pooling, 0.5 before the final dense layers) to enforce robustness.

- Classification Head: A Flatten layer followed by a Dense hidden layer (64 units) and an output Dense layer with 4 units utilizing Softmax activation for multi-class probability mapping.

## Evaluation & Metrics
The model's final performance is evaluated on the unseen test set. The notebook generates three analytical assets:
1. Accuracy and Loss Curves.
2. Confusion Matrix.
3. Classification Report.

## Tools and Libraries
This project uses:
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Tensorflow
- Split-folder
- Jupyter Notebook