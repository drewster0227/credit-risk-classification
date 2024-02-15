# Credit-risk-classification assesment report

The purpose of this analysis was to create a machine-learning classification model that when given certain features such as interest rate, borrower income, and total debt can predict if a loan is either high-risk or healthy. The predicted variable loan_status was a categorical variable with a value of 0 representing a healthy loan and a value of 1 if the loan is considered to be high-risk. 
	Logistic Regression was the chosen method for this data as it is efficient as well as handles the multicollinearity seen in this dataset very well. Resampling was performed as a secondary measure as well as the dataset provided was very heavily favored to healthy loans with relatively fewer high-risk loans. Finally a liblinear solver was used at first however the lbfgs solver created a more accurate model so that was the solver selected. 

* Machine Learning Model 1:
  * Model 1 is a logistic regression model utilizing the lbfgs solver with the following scores:

Accuracy score: 0.993
Precision healthy: 1.00
Recall healthy : 0.99
Precision high-risk: 0.85 
Recall high-risk: 0.95


* Machine Learning Model 2:
 * Model 2 is also a logistic regression model utilizing the lbfgs solver, however resampling was performed to help the model more accurately handle high-risk loan cases, here are the following scores:

Accuracy score: 0.994
Precision healthy: 1.00
Recall healthy : 0.99
Precision high-risk: 0.84 
Recall high-risk: 0.99

## Summary 
To summarize I do think these model are fairly strong as they both boast high accuracy rates, however, they both have somewhat low precision at predicting loans to be high-risk when they're actually healthy. That being said I'd select the second model as it's recall score is 99% as opposed to the 95% recall score of high-risk status. This is the more important metric compared to recall as recall is the score that demonstrates inaccuratly predicting a loan to be healthy when it is actually high-risk. This is important as the lender will want to be more confident in finding as many high-risk loans as possible in order to minimize loss and thus a model that only misses 1% of true high-risk loans seems very desirable. Therefore I would recommend usage of the second model as a method of risk-protection even though it does overpredict high-risk loans as it's better to be safe than sorry. 

