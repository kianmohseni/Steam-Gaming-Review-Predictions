# Steam Gaming User Review Predictions

## Overview

This repository contains the steam.ipynb Jupyter Notebook, which includes a comprehensive analysis of a dataset from Steam reviews. The notebook explores various machine learning techniques and data processing steps to derive insights and improve predictive modeling.

## Contents

- **steam.ipynb:** The main Jupyter Notebook containing code, visualizations, and explanations.

- **README.md:** This file, providing an overview of the project.

## Requirements

To run this notebook, you need the following dependencies:

pip install numpy, pandas, matplotlib, seaborn, scikit-learn

## Data Source

The dataset is loaded from a compressed JSON file:

https://cseweb.ucsd.edu/classes/fa24/cse258-b/files/steam.json.gz

It contains user reviews for Steam games, including user IDs, game IDs, review text, and hours played.

## Key Features

1. Data Processing

- Loads and decompresses the dataset.

- Parses JSON records into a structured format.

- Organizes data by user and game ID.

2. Feature Engineering

- Extracts features from review text.

- Computes review length as a predictive feature.

- Implements logarithmic transformation to stabilize target variable distribution.

3. Machine Learning Models

- **Linear Regression:** Predicts hours played based on review text length.

- **Outlier Removal:** Removes top 10% of extreme values to improve model performance.

- **Log Transformation:** Applies log-scaling to target variable.

- **Logistic Regression:** Classifies user engagement based on median hours played.

4. Collaborative Filtering Approaches

- **User-to-User Prediction:** Computes similarity between users based on shared game interactions using Jaccard similarity.

- **Item-to-Item Prediction:** Predicts user ratings based on similar game interactions.

- **Time-Weighted Adjustments:** Incorporates time decay factor to weight recent reviews more heavily.

5. Model Evaluation

- Implements Mean Squared Error (MSE) and Mean Absolute Error (MAE).

- Compares model performance before and after outlier removal and transformations.

- Evaluates classification models using Balanced Error Rate (BER).


## Results Summary

- Removing outliers significantly improves regression model performance.

- Log transformation stabilizes the target variable, reducing error rates.

- Logistic regression provides a robust classification model with a balanced error rate of ~0.47.

- User-to-user and item-to-item collaborative filtering approaches show strong predictive performance.

- Time-weighted adjustments improve predictions by incorporating recent activity trends.
