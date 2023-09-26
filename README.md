# credit-risk-classification
Machine learning techniques are used to analyze a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

## Overview of the Analysis
Factors considered in the analysis included data on:
* the size of the loan
* its interest rate
* the borrower's income
* the debt to income ratio
* the number of accounts held by the borrower
* any derrogatory marks against the borrower
* the borrower's total debt

The dataset (77,536 data points) was split into training and testing sets. The training set was used to build a logistic regression model using the `LogisticRegression` module from <a href=https://scikit-learn.org/stable/index.html>scikit-learn</a>. The logistic regression model was then applied to the testing dataset. The purpose of the model was to determine whether a loan to the borrower in the testing set would be low-risk or high-risk and results are summarized below.

## Results

<strong>Logistic Regression Model</strong>

* Accuracy: 94% accurate (macro average, by category), 99% based on a weighted average (by loan risk classification).
* Precision: 93% (on average).  In predicting low-risk loans, the model was 100% precise, though the model was less precise at 87% precise in predicting high-risk loans.
* Recall: 95% on average.  The model had 100% recall in predicting low-risk loans, but 89% recall in predicting high-risk loans.


## Summary

* The model does a fantastic job of predicting low-risk loans (~100% accurate).  However, if the goal of the model is to determine the likelihood of high-risk loans, the model fails to predict high-risk loans at an accuracy rate of greater than 90%.  That said, I would recommend using this model to predict the creditworthiness of borrowers, because it has well over 90% accuracy in predicting the outcome of the repayment of the initial loan. That accuracy range could be easily molded into a business risk profile to ensure sufficient capital flow for the lenders to remain in business/make a profit.