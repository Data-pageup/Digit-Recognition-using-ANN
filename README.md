# Handwritten Digit Recognition

A compact deep learning project that classifies handwritten digits (0–9) from 28×28 grayscale images. This repository implements a simple neural network pipeline including data loading, preprocessing, model training, and evaluation.

## Overview

This project demonstrates a complete workflow for a multi-class image classification task:

- Load a CSV-format digit dataset (labels + 784 pixel columns)
- Clean and normalize pixel values
- Reshape images to the required input shape
- Convert labels to one-hot format
- Train a small feedforward neural network
- Evaluate model performance on a held-out validation set

## Dataset

- **Format:** CSV with 785 columns (first column = label, remaining 784 = pixel intensities)
- **Samples:** 42,000
- **Image Size:** 28 × 28 pixels (grayscale)
- **Labels:** Digits 0–9

## Preprocessing

- Ensure pixel columns are numeric and replace missing values if any
- Normalize pixel values to the range [0, 1]
- Reshape flat pixel vectors into 28×28×1 images
- One-hot encode labels for multi-class classification
- Split data into training and validation sets

## Model

A simple neural network with:

- Input flattening stage
- Two fully connected hidden layers
- Softmax output layer for 10 classes
- Optimizer: Adam (default)
- Loss: Categorical cross-entropy
<img width="462" height="206" alt="image" src="https://github.com/user-attachments/assets/c1a6177d-5bd0-4d42-abc5-e22b39d61264" />

## Training

1. Prepare the dataset in the repository (CSV file named appropriately)
2. Run the training routine to fit the model on the training split and validate on the held-out set
3. Monitor training and validation accuracy to check learning progress

## Results

- **Validation Accuracy:** ~97%
- **Training Accuracy:** ~99%
- Indicates strong fitting with good generalization

  <img width="592" height="342" alt="image" src="https://github.com/user-attachments/assets/2895b4aa-5d2a-4e5c-8c87-cd1be654c03f" />

