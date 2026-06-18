# Customer Churn Prediction

## Overview

This project focuses on predicting customer churn using machine learning and deep learning techniques.

The goal is to identify customers who are likely to leave a service based on their demographic information, service usage, billing details, and contract characteristics.

## Dataset

The dataset contains customer information including:

* Demographic features
* Contract information
* Payment methods
* Monthly and total charges
* Service subscriptions

Target variable:

* **Churn** (Yes / No)

## Feature Engineering

Several custom features were created to improve model performance:

* Average monthly payment
* Estimated number of paid months
* Automatic payment indicator
* Senior citizen with dependents flag
* Family status indicator
* Customer stability score (`IsNoStableClient`)

Missing values in `TotalCharges` were handled and numerical conversions were applied where necessary.

## Data Preprocessing

* One-hot encoding for categorical features
* Train-test split
* Class imbalance handling using SMOTE
* Custom class weights during training

## Model

A neural network built with TensorFlow/Keras:

* Dense layer (Swish activation)
* Hidden layer (Swish activation)
* Sigmoid output layer

Training techniques:

* Early Stopping
* Learning Rate Reduction on Plateau
* Binary Cross-Entropy Loss
* Adam Optimizer

## Results

The model was evaluated using:

* Accuracy
* Precision
* Recall
* F1-score

The project demonstrates the impact of feature engineering and imbalance handling on customer churn prediction.

## Technologies

* Python
* TensorFlow / Keras
* Pandas
* NumPy
* Scikit-learn
* Imbalanced-learn

## Skills Demonstrated

* Data preprocessing
* Feature engineering
* Deep learning
* Class imbalance handling
* Model evaluation
* Binary classification
