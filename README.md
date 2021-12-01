# Home-Credit-Default-Risk-Prediction

The goal of this project is to build a machine learning model that will predict clients' repayment abilities to ensure that clients capable of repayment are not rejected and that loans are given with a principal, maturity, and repayment calendar that will empower their clients to be successful.


# About the data
The dataset, downloaded from [Kaggle](https://www.kaggle.com/c/home-credit-default-risk/overview), contain 122 variables and 307511 observations in the train set, while the test set has 48744 observations with 121 variables. This dataset has a lot of samples to train on.


## Exploratory Analysis
* Ahe dataset contains a lot of missing values. Majority of these missing values are concentrated in the apartment-based features which suggests that there is no information on where some of the clients lived. Hence these were inputed with zero. The same for features representing the number of enquiries made to the Bureau before the application.

In addition, there is a pattern to the missingness as features representing a certain characteristics have same number of missing values.

* The target variable has two distinct classes that are imbalanced. Most of the clients (91.9%) repaid their loans while 8.1% were defaulters. This implies that the target variable is imbalanced, which requires a proper crossvalidation strategy for good model evaluation.

 ![alt text](https://github.com/adeyinkaoresanya/Don-t-Overfit-Challenge/blob/main/Images/target.PNG "Distribution of the target variable")

* The distribution of income earned by the clients is skewed, which is not surprising, as well as the credit amount of the loan and loan annuity.

The age of client is normally distributed, with a typical client being 44 years old on the average.

Some errors are noticeable on the YEARS_EMPLOYED feature (-1000), which implies that a client has been employed for 1000 years. These erroenous values would be removed 

