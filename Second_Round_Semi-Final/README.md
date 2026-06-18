# AI Challenge 2025 — Image Classification (Semi-Finalist)

## Overview

This project was developed for the **AI Challenge 2025 (Semi-Final Stage)**, where the goal was to build a binary image classification model.

The task involved classifying images into two categories using deep learning methods.

Final result:

* **Rank:** 54th place (Semi-Finalist)
* **Accuracy:** ~99%

---

## Problem Statement

Given a dataset of labeled images, the goal was to predict the correct class for unseen test images.

This is a **binary image classification problem** with class imbalance and relatively complex visual patterns.

---

## Dataset

* Training images stored locally / Google Drive
* Labels provided in `train_r2.csv`
* Test set provided in `test_r2.csv`

Images were resized to:

* **360 × 360 × 3**

---

## Data Preprocessing

* Image loading using PIL
* RGB conversion
* Normalization (pixel values scaled to [0, 1])
* Image resizing to fixed resolution

---

## Handling Class Imbalance

To improve model performance on imbalanced data:

* Random Oversampling (ROS) was applied
* Class weights were used during training

This helped stabilize training and improve minority class performance.

---

## Model Architecture

A custom **VGG-style Convolutional Neural Network** was implemented using TensorFlow/Keras:

* Multiple Conv2D layers (ReLU activation)
* MaxPooling layers for spatial reduction
* Fully connected dense layers with Swish activation
* Dropout (0.6) for regularization
* Sigmoid output layer for binary classification

---

## Training Strategy

* Optimizer: Adam
* Loss: Binary Cross-Entropy
* Batch size: 32
* Epochs: up to 55
* Early stopping (patience = 50)
* Validation split: 20%

---

## Evaluation

Model performance was evaluated using:

* Accuracy
* Precision / Recall
* F1-score
* Confusion Matrix

Final performance reached approximately:

* **~99% accuracy**

---

## Key Techniques Used

* Deep CNN design (VGG-inspired)
* Image preprocessing pipeline
* Oversampling for imbalance handling
* Class weighting
* Regularization (Dropout)
* Early stopping
* Full training/validation pipeline

---

## Technologies

* Python
* TensorFlow / Keras
* NumPy
* Pandas
* Scikit-learn
* PIL (image processing)
* Matplotlib

---

## Results & Achievement

* Semi-finalist in AI Challenge 2025
* Ranked 54th place
* Achieved high classification accuracy (~99%)
* Built full end-to-end image classification pipeline

---

## What I Learned

* Designing CNN architectures from scratch
* Handling imbalanced image datasets
* Improving generalization using regularization
* Training deep learning models on real competition data
* Debugging and optimizing ML pipelines under constraints
