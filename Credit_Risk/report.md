# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
The purpose of this analysis was to assess the performance of a logistic regression model in predicting credit risk. More specifically, the model is used to distinguish between healthy loan and high-risk loads. 
* Explain what financial information the data was on, and what you needed to predict.
Features used to classify: 
1. Loan Size: The amount of money borrowed by an individual.
2. Interest rate: The percentage of price paid for borrowing the money
3. Borrower Income: Annual income earned by the individual 
4. Deb-to-income: measure of borrower's ability pays off their debts relative to their income 
5. num_of_accounts: number of banking accounts owned by individual 
6. derogatory_marks: number of negative entries in an individual’s credit report 
7. total_debt: total amount of money the individual/borrowers own 
Target:
1. Loan_status: used to classify is a healthy (0) or high-risk (1) loan candidate.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
- Checking y_label values_counts to see observe balance between healthy (0) and high-risk (1) loan candidates 
- Predictions variable carries information whether a data point is a healthy or high -risk loan based on the logistic model fitted 
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
EDA:
- Imported required libraries such as NumPy, Pandas, pathlib, scikit-learn 
- loaded lending data and reviewed data for unique patterns or observations. Split data between features (X) and labels (y)
Logistic Regression Machine Learning
- Used Logistic regression for analysis 
- split the data into training and testing set keeping random seed at 1 for easy reproducibility 
- initiated the logistic regression model and fitter the model using training data 
- Evaluated the model using balanced accuracy score as the binary classification were very different in size,
confusion matrix, and classification report.
Resampling Data: 
- Previous data had a large imbalance between the binary classification targets 
- used RandomOverSampler to correct imbalance by resampling X and Y training data 
- Retrained model using new training dataset by creating another logistic regression model 
- fitter model using resampled data and made prediction using new data 
- Evaluate the model using same metrics as before for easy comparison 
## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
  - Balanced Accuracy: 0.97 indicates that the model is doing a good job classifying between healthy and high-risk loans 
  - Precision: Measures how often you are correct. In other words, is the value truly positive. For healthy loans 0, the values were 1 which means there 
  are little to no False positive. For high-risk loans 1, the value was 0.87 which indicates there usually the prediction is correct but there is a small percentage of false positive that occur. 
  - Recall Score: measures the ability to classify all instances of high-risk loans. For healthy loans the values were 1 indicating the prediction were also right with little to no false negatives. 
  For high-risk loans the model is usually correct at classifying high-risk loans but it has a higher chance of having false negatives. 
* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  - Balanced Accuracy: 0.99 indicates that the model is doing a better job than model 1 in classifying between healthy and high-risk loans
  - Precision: Measures how often you are correct. In other words, is the value truly positive. For model 2 there was no difference from model 1 inviting the same results as before. 
  - Recall Score: measures the ability to classify all instances of high-risk loans. For healthy loans the values were 1 indicating the prediction were also right with little to no false negatives. 
  For high-risk loans the model is better classifying high-risk loans than model 1 with little to no false negatives as the score was 1. 

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s?)
Model 2 performs better as it is better at predicting high-risk loans compared to model 1. This indicated by the improvement in balanced accuracy. It is also indicated by the increase in recall score for high-risk candidates in model 2 as explained earlier in this report. In this scenario it is more important to predict the 1s as these candidates pose more of a risk for the company for who this data is being analysed. Although this model is having good accuracy, precision, and recall scores it may be worth while to use other machine learning models as this data can be less linear in nature. Also, other model may do a better job at weighting the features sued in this dataset. 



