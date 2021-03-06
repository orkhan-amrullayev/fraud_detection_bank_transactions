## Fraud Detection in Bank Transactions


The bank transactions will be used to predict fraudulent ones.

As per description of the dataset, it contains transactions made by credit cards in September 2013 by European cardholders. This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.

It contains only numerical input variables which are the result of a PCA transformation. Unfortunately, due to confidentiality issues, we cannot provide the original features and more background information about the data. Features V1, V2, … V28 are the principal components obtained with PCA, the only features which have not been transformed with PCA are 'Time' and 'Amount'. Feature 'Time' contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature 'Amount' is the transaction Amount, this feature can be used for example-dependant cost-sensitive learning. Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 otherwise.


This notebook will compare various data balancing techniques with powerful boosting models. Models used here are Random Forest, XGBoost and LGB. We will look at precision-recall curve and roc curve.
![fraud_roc](https://user-images.githubusercontent.com/64093617/141030203-f031492b-2bbd-463b-a8c1-1c0375b6dd47.png)


Content
1. Imports and reading dataset
2. Exploratory Data Analysis
3. Dealing with unbalanced dataset
- Without balancing
- Undersampling
- Oversampling

4. Building function for 3 models:

  - Random forest classifier

  - XGBoost

  - LightGBM

5. Comparison of result of the models with "Without balancing", "Undersampling", "Oversampling" options
6. Conclusion
