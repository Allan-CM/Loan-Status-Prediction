# Loan Status Prediction 

## Overview
This project focuses on predicting loan statuses using logistic regression. The analysis involves splitting the data into training and testing sets, creating a logistic regression model with the original data, and then optimizing the model by using resampled training data. The aim is to evaluate the model's performance in predicting both healthy loans (0) and high-risk loans (1).

## Technologies Used
* Python
* Pandas
* Scikit-learn
* Imbalanced-learn


## Project Structure
### Importing Libraries
* NumPy: For numerical operations.
* Pandas: For data manipulation and analysis.
* Pathlib: For handling file paths.
* Scikit-learn: For logistic regression and model evaluation metrics.
* Imbalanced-learn: For handling imbalanced datasets.

## Data Loading and Preprocessing
* Load Data: Read the lending data CSV file into a Pandas DataFrame.
* Split Data: Separate the data into features (X) and labels (y).

## Model Building and Evaluation
* Logistic Regression with Original Data:
  * Fit the logistic regression model using the original training data.
  * Evaluate the model's performance using balanced accuracy score, confusion matrix, and classification report.
* Logistic Regression with Resampled Data:
  * Use RandomOverSampler to handle the imbalanced dataset.
  * Fit the logistic regression model using the resampled training data.
  * Evaluate the model's performance on the testing data.

## Data Analysis Steps
1. Data Loading and Preprocessing: Load the lending data and separate it into features (X) and labels (y).
2. Logistic Regression with Original Data: Fit the logistic regression model using the original training data. Evaluate the model's performance using metrics like balanced accuracy score, confusion matrix, and classification report.
3. Logistic Regression with Resampled Data: Use RandomOverSampler to oversample the minority class, fit the logistic regression model using the resampled training data, and evaluate the model's performance on the testing data.

## Results and Insights
### Original Data
* Balanced Accuracy Score: 97.21%
* Classification Report:
  * Precision, Recall, and F1-score are high for healthy loans (0).
  * For high-risk loans (1), precision is lower, but recall and F1-score are still acceptable.
### Resampled Data
* Balanced Accuracy Score: 99.60%
* Classification Report:
  * Precision remains the same for healthy loans (0).
  * For high-risk loans (1), recall and F1-score improve significantly, reaching 100% recall.

## Conclusion
The logistic regression model performs well in predicting loan statuses, especially after oversampling the minority class to handle the imbalanced dataset. The resampled model shows a significant improvement in predicting high-risk loans with no false negatives, making it more reliable for practical applications.

## Repository Organization
1. credit_risk_classification --> Contains python script for the credit-risk-classification data anaylsis for this assignment 
2. Report --> Contains Credit risk Analysis Report 
3. Resource Folder --> Contains leadning data csv used for this analysis

## Credits: 
https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.RandomOverSampler.htmls. --> Used resource to learn how to address the imbalance in target data classificiation using random resampler 
