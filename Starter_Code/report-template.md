# Report Template-credit-risk-classification
![image](https://github.com/Marce1301/credit-risk-classification/assets/119386031/85093334-ffd3-4257-9118-05ef76d6beea)

## Overview of the Analysis

The purpose of this analysis is to evaluate a model based on loan risk, using a dataset of historical lending activity from a peer-to-peer lending services company that will help to build the model that can identify the creditworthiness of borrowers.

Dependant variable (y value) in this analysis was the "loan status" indicating if a loan is healthy or at risk.
Independent Variables (x values) were loan size, interest rate, borrower income, debt to income ratio, number of accounts and derogatory marks.

In this analysis, I first split the data to traning and test sets. Then I defined the dependent and independent variable and I created logistic regression model and fit the original data to this model. Trained model was used to make predictions. Finally, I evaluated the model`s performance.

Two diffeent Logistic Regression models were created by using the original data set and randomy over resampled data set (to get rid of the imbalances). In the end, their results -which was gathered with scikit-learn library- were compared.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Logistic Regression Model with Original Data

![image](https://github.com/Marce1301/credit-risk-classification/assets/119386031/78d589b2-dbc1-40c0-bf5c-36988d874992)

 Accuracy, Precision, and Recall scores.

![image](https://github.com/Marce1301/credit-risk-classification/assets/119386031/5b3c60e1-5aff-42e5-a0ff-cea3c02f8c5e)

* Logistic Regression Model with Randomly Oversampled Data

![image](https://github.com/Marce1301/credit-risk-classification/assets/119386031/e3004fc2-2df3-49ba-8599-96c9db698e03)

 Accuracy, Precision, and Recall scores.

![image](https://github.com/Marce1301/credit-risk-classification/assets/119386031/d0d7e65c-4b36-4857-a8e7-e65511781a41)

## Summary

The lending company aims to accurately classify healthy and non-healthy loans to minimize potential costs. Misclassifying healthy loans as non-healthy can result in the loss of customers, while misclassifying non-healthy loans as healthy can lead to financial losses. To address this, two logistic regression models were compared: one trained on imbalanced data and another trained on oversampled (balanced) data.

The model fitted with oversampled data outperformed the model trained on imbalanced data. It achieved higher accuracy and recall scores, indicating fewer mistakes in classifying non-healthy loans. The confusion matrices for both models provide insights into the number of correct and incorrect predictions for healthy and non-healthy loans.

For the model trained on imbalanced data:

False positives: 56 cases (actual healthy loans classified as non-healthy)
False negatives: 102 cases (actual non-healthy loans classified as healthy)
For the model trained on balanced data (oversampled):

False positives: 4 cases (actual healthy loans classified as non-healthy)
False negatives: 116 cases (actual non-healthy loans classified as healthy)
The drastic reduction in false positives in the model trained on balanced data suggests that it is better at correctly classifying both healthy and non-healthy loans. Therefore, it is recommended to use the logistic regression model fitted with balanced (oversampled) data.

The analysis emphasizes the importance of addressing the imbalance in the dataset through oversampling. By doing so, the model achieves better accuracy and recall, enabling more accurate predictions for both healthy and non-healthy loans. This helps in minimizing the costs associated with false positives and false negatives.
