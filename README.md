# Credit Risk Classification using Logistic Regression

## Overview of Analysis

The purpose of this analysis is to create a model which identifies High Risk Loans using a Logistic Regression Machine Learning.  The input data includes records of loans, detailing the loan's size and interest rate, as well as the applicant's debt to income ratio, number of accounts, derogatory marks, and more.  This training data also contains whether each loan is Healthy or High Risk.  In this data set, there are approximately 75,000 Healthy loans and 2,500 High Risk loans, meaning the target classes are highly imbalanced. 

For this analysis, two Logistic Regression models were developed.  One was trained on a stratified subset of the data, and the other was trained on a subset whose classes were balanced using Random Oversampling.  The models were then given sets of test data and their performances were evaluated using a confusion matrix and classification report. 

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Balanced Accuracy Score: 0.94426
  * Healthy Loan Precision: 1.00
  * Healthy Loan Recall: 1.00
  * High Risk Loan Precision: 0.87
  * High Risk Loan Recall: 0.89



* Machine Learning Model 2:
  * Balanced Accuracy Score: 0.996
  * Healthy Loan Precision: 1.00
  * Healthy Loan Recall: 1.00
  * High Risk Loan Precision: 0.87
  * High Risk Loan Recall: 1.00

## Summary

Overall, Model 1 has very high accuracy, and is perfectly precise when identifying healthy loans.  However, of the loans flagged as High Risk, only 87% were actually High Risk.  Also, the model only correctly identified 89% of all High Risk Loans (recall) in the test set.  Depending on the average cost of a defaulted loan and our tolerance to those losses, the recall and precision values may be too high for the model to be usable.

Model 2 is also able to predict Healthy Loans with near perfection.  Of its High Risk Loan determinations, only 87% were correct (precision), however it did correctly identify every High Risk Loan in the test set (recall).  This is a great improvement on our first model, as we have the same precision in identifying High Risk Loans, but are much less likely to miss a High Risk Loan.

For the purposes of correctly flagging all High Risk Loans, the second model is highly preferable and may be suitable for industry use.  However, additional consideration should be given to the 87% precision in correctly flagging risky loans, as the cost of rejecting healthy loan applications may actually be higher than that of accepting risky loans.  Future analysis may look at improving the precision of the second model, or potentially using a different machine learning model altogether, such as a decision tree algorithm.

## Authorship
Data for this project was provided by the UNC Data Analytics Bootcamp.  This report and all code for the regression model were written by Sam Lind.
