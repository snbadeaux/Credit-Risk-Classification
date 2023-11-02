# Credit-Risk-Classification
Machine learning techniques such as logistic regression, are used to analyze a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.<br>

# Overview

   The factors considered in this analysis included the size of the loan, interest rate, the borrower's income, the debt-to-income ratio, the number of accounts the borrower holds, derogatory marks against the borrower, and total debt. All these factors, together, were set as the independent variable (X). After training the model, with around 70% of the data, we ask it to predict y, which we set up as loan status. The loan status column contains either a 0 or a 1, where 0 means the loan is healthy, and a 1 means that the loan is at a high risk of defaulting. <br>

   Two models were run, the first of which used logistic regression and only sampled the data points once to predict an outcome. The second model used some of the data points more than once, with the Random Over Sampler technique, in order to balance the counts of the minority class, which in this case was 1 (high-risk loans). We called this data, Resampled Data. Logistic Regression was then also used in order to predict an outcome, with the hopes that the overall accuracy would increase.


# Results
Machine Learning Model 1:<br>
1. Overall Accuracy: 0.99.
2. Precision: for healthy loans, the precision is 1.00, for high-risk loans, the precision is 0.87.
3. Recall: for healthy loans, the recall score is 1.00, for high-risk loans, the recall score is 0.89.
4. F1-Score: for healthy loans, the f1-score is 1.00, for high-risk loans, the f1-score is 0.88.<br>

   
Machine Learning Model 2 (Resampled Data):<br>
1. Overall Accuracy: 1.00.
2. Precision: for healthy loans, the precision is 1.00, for high-risk loans, the precision is 0.87.
3. Recall: for healthy loans, the recall score is 1.00, for high-risk loans, the recall score is 1.00.
4. F1-Score: for healthy loans, the f1-score is 1.00, for high-risk loans, the f1-score is 0.93.<br>

# Summary
The resampled logistic regression model predicts a healthy, low-risk loan with 100% precision. It predicts a high-risk loan with lower precision at 87%. The balanced accuracy of the model is 100%. Overall, the classification report stayed relatively the same, even with the oversampling actions of trying to improve the minority class predictive performance. The only thing that truly changed, with any significance, was the balanced accuracy score. It went from 99% to 100%. However, this could possibly be due to overfitting. More cross-validation techniques would need to be used in order to verify these predictive outcomes.<br>

Model 2 is less likely to predict false negative results. However, based on the confusion matrices for each model, Model 2 predicted slightly more false positives (low-risk when the actual was high-risk).<br>

If the goal of the model is to determine the likelihood of high-risk loans, neither model scores above 90% precision. Model 2 had fewer false predictions of the testing data overall and would be the best model to use based on the high accuracy and recall of this model.

# Sources
1. Dataset provided by edX Boot Camps LLC
2. ChatGPT https://chat.openai.com/

