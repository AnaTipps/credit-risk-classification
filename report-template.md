# Module 20 Report
![image](https://github.com/AnaTipps/credit-risk-classification/assets/131827518/238dbc95-4420-459d-b870-8be2c114812f)

## Overview of the Analysis

- The purpose of this analysis was to predict the risk of a loan based on financial information on the loan and borrower such as the loan size, interest rate, and  borrower income, dept, number of accounts, deragotary marks and total debt. The models were trained using different methods, and their performances were compared to determine the better-performing model. The predictive variables in the model are the labels 0 (healthy loan) and 1 (high-risk loan).

In the process of building the models, the dataset was split into features and labels, and further divided into training and testing sets.

- Stages of Machine Learning: 
  + Data Preparation: Read data, Separate Labels and Features, Split Training and Test data, Resample Training data using RandomOverSampler (second model only)
  + Machine Learning Models Preparation: Create instance of a logistic regression model, fit the training data to the model, predict the outcome using test data.
  + Model Evaluation: Create confusion matrix and classification reports to evaluate model performance.
    * Machine Learning Model 1 was built using Logistic Regression supervised machine learning model used for classification tasks, where the goal is to predict a binary outcome Uses a logistic function to transform a linear combination of input variables into a probability of belonging to one of the two classes.
    * Machine Learning Model 2 used the RandomOverSampler a module from imblearn that increases the number of samples in the minority class by randomly replicating existing samples to balance class distribution.
  


## Results

### Machine Learning Model 1:
* Accuracy: The classification model correctly predicted 94.4% of the samples, considering both the minority and majority class, taking into account the class imbalance of the dataset.
* Confusion matrix:
   - **18,679** out of **18,759** healthy loans or true negatives correctly predicted
   - **80** out of **18,759** false positives
   - **558** out of **625** high risk loans or true positives correctly predicted
   - **67** out of **625** false negatives
* Classification Report:
   - Precision: Majority of healthy loans predicted are correct, **87%** of high-risk loans predicted are high-risk loans.
   - Recall: Majority of actual healthy loans were correctly predicted, **89%** of actual high-risk loans were predicted as high risk.

### Machine Learning Model 2:
* Accuracy: The classification model correctly predicted 99.6% of the samples, considering both the minority and majority class, taking into account the class imbalance of the dataset.
* Confusion matrix:
   - **18,668** out of **18,759** healthy loans or true negatives correctly predicted
   - **91** out of **18,759** false positives
   - **623** out of **625** high risk loans or true positives correctly predicted
   - **2** out of **625** false negatives
* Classification Report:
  - Precision: Majority of healthy loans predicted are correct, **87%** of high-risk loans predicted are correct.
  - Recall: Majority of actual healthy loans were correctly predicted; Majority of actual high-risk loans were predicted as high risk.

## Summary
In summary, for Machine Learning Model 1,  the chance that the model identifies an actual healthy loan as high risk is low; however, the chance that the model predicts a high-risk loan as healthy is approximately **11%**.

The model is better in at predicting healthy loans, compared to its ability to predict high risk loans, and is more likely to give a false negative (miss a high-risk identification) than it is to give a false positive (wrongly identify a healthy loan as high risk).

In summary, for Machine Learning Model 2, the chance that the model identifies an actual healthy loan as high risk or a high-risk loan as healthy are both low now, less than **0.5%** of the time.

The model performs like the un-sample previous version in predicting healthy loans, however, it significantly improved in terms of predicting un-healthy loans, and the chances that it wrongly identifies a loan is similar for each category and relatively small.
