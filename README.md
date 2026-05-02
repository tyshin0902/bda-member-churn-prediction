# BDA Member Churn Prediction

A machine learning project for predicting BDA member withdrawal using member profile, activity, and participation-related data.

## Overview

This project aims to predict whether a BDA member is likely to withdraw from the organization.  
The main goal is not only to build a classification model, but also to understand which types of member information may be useful for identifying potential churn risk.

The project follows a typical machine learning workflow:

1. Exploratory Data Analysis
2. Data preprocessing
3. Model training
4. Hyperparameter tuning
5. Model evaluation

## Problem Definition

Member churn prediction is a binary classification task.

- **Target variable:** `withdrawal`
- **Positive class:** member withdrew
- **Negative class:** member did not withdraw

The dataset is imbalanced, so the project uses **F1 score** as the main evaluation metric instead of relying only on accuracy.

## Dataset

The original training dataset contains:

- **Train data:** 1,056 rows and 46 columns
- **Test data:** 788 rows and 45 columns

The dataset includes member-related information such as:

- School and major information
- Job status
- Re-registration status
- Previous class participation
- Project preference
- Time input
- Contest participation
- Career or learning-related survey responses

After preprocessing, the final training data contains:

- **Processed features:** 24
- **Target distribution:**
  - `withdrawal = 1`: 730
  - `withdrawal = 0`: 326

## Project Structure

```text
bda-member-churn-prediction/
├── data/                         # Raw and processed dataset files
├── 01_EDA.ipynb                  # Exploratory data analysis
├── 02_Preprocessing.ipynb        # Data cleaning and feature preprocessing
├── 03_Modeling.ipynb             # Model training, tuning, and evaluation
├── 04_Additional_Analysis.ipynb  # Additional experiments and analysis
├── requirements.txt              # Required Python packages
└── README.md                     # Project documentation