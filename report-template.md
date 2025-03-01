# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).
* The purpose of this analysis was to identify how good a logistic regression model was at identifying high risk versus safe loans and how likely those loans were to default. The model looked at the size of the loan, interest rate, income of the borrower, the ratio of debt to income, number of loans, total debt, and if the number of deragatory marks there were. The variable the model was trying to predict if a loan defaulted or not based off of the variables listed above. To create my model, I separated the data into two variables. My y variable was loan status, why was 0 for the loan did not default, 1 being the loan did default. My X variable was the rest of the data in the dataframe. I then split the data using train_test_split and created a logisitic regression model and fit the model with the X_train and Y_train data. I then created a data frame where the model used the X_test data to see the prediction of the loan vs the actual result of the loan. I then created a confusion matrix and classification report to visualize the total number of predictions and see the precision and recall of the model for identifying safe loans and high risk loans.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * The logisitic regression model had phenomenal results predicting which loans would not default. With a precision of 1.0 and a recall of .99 there were only 110 instances out of 18755 total loans where the model thought it would default and it ended up being a safe loan. When it came to predicting which loans would default the model hada precision of .84 and a recall of .94. There were 36 false negatives predicted out of 619 total defaulting loans. The model while stil respectable, was much more concerning in this regard as 16% of the time it missed a loan that would end up defaulting. Overall, the accuracy of the logistic regression model was 99% for correctly predicting loans. 

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* I would not recommend using this logistic regression model for finding loans that are high risk. While it did a great job of predicting which loans are safe, 16% of the time it predicted a loan was safe and it ended up defaulting. Because banks give out lots of loans, 16% of them being false negatives could cause big issues for the company. Limiting false positives is important but if we predict a loan is unsafe and it ends up being safe that does not effect the company's bottom line as much as predicting a loan is safe and it ends up not being safe. The model may get better as we add more data to it for it to learn from but at this time there is too much risk with the model. 
