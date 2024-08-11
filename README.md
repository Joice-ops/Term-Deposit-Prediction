# Term Deposit Prediction :bank:

## Overview 
This project aims to predict whether a customer will subscribe to a term deposit based on data from direct marketing campaigns conducted by a Portuguese banking institution. Accurate predictions in this domain are critical for optimizing marketing strategies, reducing business losses, and protecting customer relationships.

## Project Background
The data used in this project is sourced from the [UC Irvine Machine Learning Repository](https://archive.ics.uci.edu/dataset/222/bank+marketing), comprising 45,211 instances. The data reflects the substantial effort involved in contacting clients via phone calls, often multiple times, to determine whether they would subscribe to a term deposit. Inaccurate predictions, particularly false positives (predicting a non-subscriber as a subscriber), can lead to wasted resources and strained customer relationships.

## Problem Statement
A significant challenge in this project is the high number of false positives, where the model incorrectly predicts non-subscribers as subscribers. This misclassification is costly, leading to inefficient allocation of marketing resources and potentially damaging customer relations. The project's goal is to develop models that minimize these false positives, especially given the imbalanced nature of the dataset.

## Objectives :dart:
- Develop predictive models that minimize false positives.
- Improve precision and recall rates for predicting non-subscribers.
- Optimize resource allocation and enhance marketing strategies in the banking sector.

## Dataset
- **Source:** [UC Irvine Machine Learning Repository](https://archive.ics.uci.edu/dataset/222/bank+marketing)
- **Features:** 16
- **Instances:** 45211
- **Stratification**: The data was stratified by feature 'job' to achieve a 0.75/0.25 split between the classes, instead of the original 0.9/0.1, to better balance the dataset.

## Outlier Detection
To address potential noise in the data, DBSCAN was used to identify and remove outliers. However, this step did not significantly impact the final model's performance.

## Models Evaluated 
Three machine learning models were evaluated with following metrics in this project:
- Confusion Matrix
- Classification Report
- Precision-Recall (PR) Curve
- Receiver Operating Characteristic (ROC) Curve

1. Logistic Regression
- Accuracy: 0.79
- Class 1 (Subscribers):
  - Precision: 0.75
  - Recall: 0.24
2. Support Vector Machine (SVM)
- Accuracy: 0.79
- Class 1 (Subscribers):
  - Precision: 0.83
  - Recall: 0.19
3. Random Forest
- Accuracy: 0.79
- Class 1 (Subscribers):
  - Precision: 0.60
  - Recall: 0.38
After thorough analysis, the Support Vector Machine (SVM) model outperformed the other two models in key performance metrics, particularly in minimizing false positives.

## Insights
- The dataset is imbalanced, with a higher number of non-subscribers compared to subscribers, making it challenging to achieve high precision and recall rates for non-subscribers.
- False positives are particularly costly in this context, leading to inefficient marketing efforts and potential harm to customer relationships.
- The SVM model was identified as the best-performing model for this problem.

## Files
- TermDepositmodel.joblib: The saved final SVM model.
- preprocessor.pkl: The data preprocessing pipeline used for the model.
- bank-full.csv: The dataset used for this project
