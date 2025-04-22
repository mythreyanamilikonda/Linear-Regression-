# Overview

In this assignment, you will explore a dataset containing over one million personal loans
originated between 2008 and 2017 on LendingClub. The dataset includes detailed loan
characteristics (e.g., interest rate, loan amount), borrower characteristics (e.g., FICO score,
income), and loan outcomes (e.g., early default and return). Your task is to analyze the dataset,
build linear models, and make predictions of returns on the test set.


## Description

Requirements

# 1. Exploratory Data Analysis
Perform exploratory data analysis to understand the patterns and relationships within the dataset. Your analysis should include:

Report the summary statistics, such as average, minimum, maximum, for key variables.
Histograms, scatter plots, and box plots for key variables.
Correlation plots to assess relationships between features.

# 2. Data Preprocessing

# 2.1 Sampling**
You are required to further sample the training data into training and validation sets.

# 2.2 Handling Missing values
Missing data is present in the dataset. You may choose to either impute missing values or filter out incomplete observations. Justify your choice of approach (e.g., forward filling, backward filling, or mean).

# 2.3 Feature Engineering
Generate at least one interaction term and one nonlinear (e.g., quadratic) term. Provide justification for the chosen interaction/nonlinear terms and examine whether they are statistically significant in your model.
Scale the numerical features using either standardization or normalization techniques. Explain how it improves the dataset for machine learning models.
Apply one-hot encoding and label encoding to transform qualitative features into numerical features.

# 3. Model

# 3.1 Linear Regression Model

Fit a simple linear regression model to predict the loan return. Report the in-sample and out-of-sample R-squared.

# 3.2 Regularized Regression Model: Lasso Regression, Ridge Regression, and Elastic Nets
Fit Lasso regression, Ridge regression, and Elastic Nets to predict the loan return. Select the hyperparameters using the results in the validation set. Report the in-sample and out-of-sample R-squared.

# 4. Predicting on the Test Set
Use your best regression (including the hyperparameters) to predict the outcomes for the test set (lc_loan_test.csv). Replace the values in submission_test.csv for the columns:

return: Your regression predictions for loan returns.
Make sure the predictions match the ‘id’ column to ensure correct evaluation.
For submission details, please refer to Rules section
Evaluation
Submissions are evaluated on R2 between the predicted return and the observed return.

where benchmark is 0

Submission File
Refer to 'sample_submission.csv' for your test set predictions. It includes the following columns:

id: Unique loan identifier (to match loans in lc_loan_test)
return: Placeholder for your predictions for loan returns. The column is filled with 0
id,return
1,0.1
2,0.15
3,-0.1
etc.
