# Home-Credit-Default-Risk-Prediction

The goal of this project is to build a machine learning model that will predict clients' repayment abilities to ensure that clients capable of repayment are not rejected and that loans are given with a principal, maturity, and repayment calendar that will empower their clients to be successful.


# About the data
The dataset, downloaded from [Kaggle](https://www.kaggle.com/c/home-credit-default-risk/overview), contain 122 variables and 307511 observations in the train set, while the test set has 48744 observations with 121 variables. This dataset has a lot of samples to train on.


## Exploratory Analysis
* The dataset contains a lot of missing values. Majority of these missing values are concentrated in the apartment-based features which suggests that there is no information on where some of the clients lived. Hence these were inputed with zero. The same for features representing the number of enquiries made to the Bureau before the application.

In addition, there is a pattern to the missingness as features representing a certain characteristics have same number of missing values.

* The target variable has two distinct classes. Most of the clients (91.9%) repaid their loans while 8.1% were defaulters. This implies that the target variable is imbalanced, which requires a proper crossvalidation strategy for good model evaluation.

 ![alt text](https://github.com/adeyinkaoresanya/Don-t-Overfit-Challenge/blob/main/Images/target.PNG "Distribution of the target variable")

* The distribution of income earned by the clients is skewed, which is not surprising, as well as the credit amount of the loan and loan annuity.

* The age of client is normally distributed, with a typical client being 44 years old on the average.

* Most of the defaulters had no children, did not provide work phone, or email address and could not be reached on their mobile phones.

* There are more male clients than female, however, more of the defaulters were female. Most of the clients didnt own a house and tookout cash loans.


## Data Preprocessing and Feature Engineering

Custom transformers were built using Sklearn pipeline to transform the variables, input missing values, generate new features, eliminate skewness and scale the features.

## Model Building and Evaluation

*	Out of six models that were built, LGBM had a higher local validation score but catboost algorithm achieved a higher score on the private leaderboard(0.72958)c

![alt text](https://github.com/adeyinkaoresanya/Don-t-Overfit-Challenge/blob/main/Images/Models_table.PNG "Models")
