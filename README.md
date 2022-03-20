# fintech_challenge_12
This challenge uses historical lending activity data in order to predict the borrower's credit health. This notebook includes two LinearRegression models, 
one model without overfitting and one with overfitting.

---
## Technologies
This program utilizes Jupyter Lab with the following libraries:
![](screen_cap/imports.PNG)

---
# Project Report

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge.

The purpose of this analysis is to create two LogisticRegression models that can accurately predict borrower's credit health. We use a dataset that includes borrower 
information that will help our models make predictions.

For our dataset, we use a csv file with historical lending activity data, this contains borrower information such as:
*loan_size
*interest_rate
*borrower_income
*debt_to_income
*num_of_accounts
*derogatory_marks
*total_debt
*loan_status

We use this data inside of our model to predict 'loan_status'. Remember, the goal of this challenge is to create two models which predicts borrower's credit health so 
targetting the 'loan_staus' feature is our best bet. A 'loan_status' of 1 reflects a high-risk loan, and a 'loan_status' of 0 reflects a healthy loan.

For our LinearRegression models we use model, fit, predict to produce the balanced accuracy score, confusion matrix, and the classification report.
The first model uses the data in its original form, while the second model uses oversampling to randomly select values and help balance the dataset.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Logistic Regression:
	*Balanced Accuracy Score: 95.2%
	*Precision: Healthy-1.0  Risky-0.85
	*Recall: Healthy-0.99  Risky-0.91

* Logistic Regression with Oversampling:
	*Oversampled Balanced Accuracy Score: 99.4%
	*Precision: Healthy-1.0  Risky-0.84
	*Recall: Healthy-0.99  Risky-0.99

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

The oversampled model seems to perform better than the first model. I believe it is the better model because the recall jumps from 0.91 to 0.99 for risky borrowers.
In this domain, '0' or risky borrowers is priorized since the company can simply perform a manual analysis if someone is flagged. The oversampled model does a good job
raising risky borrowers recall while maintaing a recall of 0.99 for healthy lenders. Overall I would recommend the oversampled model since it protects against risky borrowers
effectively.

---
## Contributors
Kevin Gross

---
## License
This program is covered under the MIT license.