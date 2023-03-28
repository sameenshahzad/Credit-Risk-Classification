# Credit-Risk-Classification

## Background
In this challenge, I used various techniques to train and evaluate a model based on loan risk. I used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers

The analysis was performed in the following subsections:

* Split the Data into Training and Testing Sets
* Create a Logistic Regression Model with the Original Data
* Predict a Logistic Regression Model with Resampled Training Data


## Overview of the Analysis

The purpose of this analysis is to use Machine Learning to analyze a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers

Under this analysis, we will predict which loans are healthy (low-risk) or non-healthy (high-risk) based on the loan status provided by the lending company.

Taking a look at the dataset and using the value_counts fuction, we were able to identify that the data was highly imbalanced; more Healthy Loans [0] and less non-Healthy Loans [1]

We crteated a Logistic Regression Model with the original data (Machine Learning Morel 1) and evaluated the model's performance by: 
- calculating the accuracy score of the model.
- Generating a confusion matrix.
- Printing the classification report

To generate a higher accuracy score and better train the model, we used RandomOverSampler module from the imbalanced-learn library to resample the data and obtain a balanced dataset.

We then created Logistic Regression Model with resampled data to fit the model (Machine Learning Morel 2) and evaluated the model's performance by: 
- calculating the accuracy score of the model.
- Generating a confusion matrix.
- Printing the classification report


## Results

* Machine Learning Model 1:
  * Balanced Accuracy Score: 0.95
  * Precision: the model predicted healthy loans [0] 100% of the time and predicted non-healthy loans [1] 84% of the time.
  * Recall scores: the model made 1% of mistakes when predicting healthy loans and made 9% of mistakes when predicted non-healthy loans


* Machine Learning Model 2:
  * Balanced Accuracy Score: 0.99
  * Precision: the model predicted healthy loans [0] 100% of the time and predicted non-healthy loans [1] 85% of the time.
  * Recall scores: the model made 1% of mistakes when predicting healthy loans and made 1% of mistakes when predicted non-healthy loans

## Summary

* The Logistic Regression model fitted with OverSampled data performs  better than the model fitted with Imbalanced data. This is due to the balanced data being used for the model and generating a higher accuracy score and a higher recall. 

* Model 2 prediction are more accurate than Model 1, such that there are fewer mistakes when classifying non-healthy loans. 

* Based off of this analysis, we would recommend using Model 2 (Logistic Regression Model fitted with Balanced (oversampled) data.

