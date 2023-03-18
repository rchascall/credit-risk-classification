# Loan Risk Model Evaluation
This repository contains code and data for training and evaluating a machine learning model based on loan risk. The goal of this project was to use historical lending activity data from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

## Data
The data used for model creation was a CSV file containing a dataset of historical lending activity. 

## Model Training and Evaluation
The following techniques were used to train and evaluate the model:

1. Splitting the data into training and testing sets.
2. Creating a logistic regression model with the original data.
3. Creating a logistic regression model with resampled training data.

Two classification reports were generated to evaluate the performance of the model, one using the original data and the other using resampled data. The classification reports are as follows:

#### Original Data Classification Report
| .        | precision | recall | f1-score | support |
| -------- | ----------| -------| ---------|---------|
|        0 | 1.00      | 1.00   | 1.00     | 18759   |
|        1 | 0.87      | 0.89   | 0.88     | 625     |  
| -------- | ----------| -------|----------|---------|
| accuracy |           |        | 0.99     | 19384   |
| macro avg| 0.94      | 0.94   | 0.94     | 19384   |
| weighted | 0.99      | 0.99   | 0.99     | 19384   |

#### Resampled Data Classification Report
| .        | precision | recall | f1-score | support |
| -------- | ----------| -------| ---------|---------|
|        0 | 1.00      | 1.00   | 1.00     | 18759   |
|        1 | 0.87      | 1.00   | 0.93     | 625     |  
| -------- | ----------| -------|----------|---------|
| accuracy |           |        | 1.00     | 19384   |
| macro avg| 0.94      | 1.00   | 0.96     | 19384   |
| weighted | 1.00      | 1.00   | 1.00     | 19384   |

The confusion matrices were also used to show the performance of the models as follows:

#### Original Data Confusion Matrix
|          | Actual Pos  | Actual Neg |
|----------| ------------|------------|
| Predicted| 18679       | 80         |
| Pos      |             |            |
|----------|-------------|------------|
| Predicted| 67          | 558        |
| Neg      |             |            |
|----------|-------------|------------|         

#### Resampled Data Confusion Matrix
|          | Actual Pos  | Actual Neg |
|----------| ------------|------------|
| Predicted| 18668       | 91         |
| Pos      |             |            |
|----------|-------------|------------|
| Predicted| 2           | 623        |
| Neg      |             |            |
|----------|-------------|------------|  


## Conclusion
The results show that resampling the data improved the performance of the model as it relates to predicting the high-risk loans.  However, false positives did result in a slight reduction of accuracy as it relates to the healthy loans.  Even so, the model using the resampled data clearly performed better.  
