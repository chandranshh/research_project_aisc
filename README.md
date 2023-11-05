# Breast Cancer Diagnosis Using Logistic Regression

## Overview

This repository contains code and a logistic regression model for breast cancer diagnosis. We use a breast cancer dataset with cell nucleus characteristics to build a model that classifies cases as either benign or malignant. The code implements data preprocessing, feature selection, model building, and evaluation.

## Table of Contents

- [Dataset](#dataset)
- [How it Works](#how-it-works)
  
## Dataset

The dataset used in this project contains cell nucleus characteristics, including radius, texture, smoothness, and more. The target variable is the diagnosis, which can be either 'M' for malignant or 'B' for benign. We've used this data to build a logistic regression model for breast cancer diagnosis.

## How it Works

### Data Preprocessing

1. **Loading the Dataset**: We start by loading the breast cancer dataset using Pandas.

2. **Checking for Missing Values**: We check for missing values in the dataset and remove any columns with missing entries.

3. **Visualizing Class Distribution**: We visualize the class distribution to understand the balance between benign and malignant cases.

### Data Cleaning

1. **Removing 'Worst' Columns**: We eliminate columns associated with "worst" attributes to simplify the model.

2. **Eliminating 'Perimeter' and 'Area' Columns**: Columns related to "perimeter" and "area" attributes are removed to reduce multicollinearity.

3. **Dropping 'Concavity' and 'Concave Points' Columns**: Columns related to "concavity" and "concave points" attributes are removed, considering them potentially redundant.

### Model Building

1. **Splitting the Dataset**: The dataset is split into training and testing sets (70-30) to train and evaluate the model separately.

2. **Defining the Logistic Regression Model**: We create a logistic regression model using the Statsmodels library and define the model using a formula that includes the selected features.

3. **Fitting the Model**: We fit the logistic regression model to the training data, allowing the model to learn the relationships between the features and the target variable.

### Model Evaluation

1. **Predicting Test Data**: The trained model is used to predict the test data, assigning probabilities to each case.

2. **Converting Probabilities to Categorical Labels**: Probabilities are converted into categorical labels using a threshold of 0.5: closer to 0 is "Malignant" (M), and closer to 1 is "Benign" (B).

3. **Displaying Classification Report**: We present a classification report with precision, recall, and F1-score, assessing the model's classification accuracy.

4. **Calculating and Displaying the Confusion Matrix**: The confusion matrix helps evaluate the model's performance by counting true negatives, false positives, false negatives, and true positives.

5. **Calculating the Percentage of Correct Predictions**: We calculate the percentage of correct predictions to provide an overall measure of model accuracy.
