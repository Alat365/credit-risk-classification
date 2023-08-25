# credit-risk-classification

## Overview of the Analysis

In this analysis, we are looking at a dataset that contains the following information:

* Loan Size
* Interest Rate
* Borrower Income
* Debt to Income
* Number of Accounts
* Derogatory Remarks
* Total Debt
* Loan Status

Given this data, we want to predict whether an individual would be considered high-risk borrowers or not when deciding if they would be ideal customers in a peer-to-peer lending services company. When looking at the `value_counts` of the original data, it appears that a majority of individuals fell under the "Healthy Loan (0)" category while only a small portion of individuals fell under the "High-Risk Loan (1)" category. 

After training a Logistic Regression model, the original data was resampled using `RandomOverSampler` in order to fit the original dataset to where each label (Healthy vs. High-Risk) contained the same number of data points as compared to the original which was previously mentioned to lean heavily towards a higher number of Healthy Loans. With this newly resampled data, another Logistic Regression was ran to make predicitons as well.

## Results

### Machine Learning Model 1:
  * Accuracy: `99%`
  * Precision:
    * Healthy Loan (0): `100%`
    * High-Risk Loan (1): `85%`
  * Recall scores:
    * Healthy Loan (0): `99%`
    * High-Risk Loan (1): `91%`

### Machine Learning Model 2:
  * Accuracy: `99%`
  * Precision:
    * Healthy Loan (0): `100%`
    * High-Risk Loan (1): `84%`
  * Recall scores:
    * Healthy Loan (0): `99%`
    * High-Risk Loan (1): `99%`

## Summary

When looking at the results of the classification report, it appears that both models are relatively similar with minor differences in value. From the values above, it is shown that the biggest difference in results was in the Recall scores for "High-Risk Loan" individuals. From our analyis, it appears that the second machine learning model has a higher advantage given that it has a higher recall score of `99%` for High-Risk Loans yet only loses in precision by `1%` when compared to the first machine learning model.