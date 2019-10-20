# LoanPrediction
A dataset of 495,242 loans with 144 recorded variables was explored and a machine learning model was trained to predict whether someone would default on their loan.

The final model was a random forest classifier, which obtained 82% accuracy, an AUC of 0.90 and an F1 score of 0.85.


## Dataset:
Four CSV files available here:
[Loans2018Q1](https://www.dropbox.com/sh/yxyf0v1crwtutw0/AAC6J6W03TMF_GhqBx6i4tCfa/LoanStats_2018Q1.csv?dl=0),
[Loans2018Q2](https://www.dropbox.com/sh/yxyf0v1crwtutw0/AABfpZwLzsb6CcuD85bflUI-a/LoanStats_2018Q2.csv?dl=0),
[Loans2018Q3](https://www.dropbox.com/sh/yxyf0v1crwtutw0/AABZnH1MpTd-gEr4MywoMcJCa/LoanStats_2018Q3.csv?dl=0),
[Loans2018Q4](https://www.dropbox.com/sh/yxyf0v1crwtutw0/AAB8sPPalpxHnBW48JARNpYqa/LoanStats_2018Q4.csv?dl=0).


## Summary of process:
#### Exploratory analysis of dataset:
- dimensions
- variables
- missing data
- relationships between loan size, loan grade, purpose of loan, property ownership and application type

#### Preprocessing data for model development:
- removing empty columns
- removing columns with large percentage of missing data
- modifying data types
- label encoding of strings to numerical
- creating dummy variables for low cardinality variables
- creating bins for loan amount and annual income
- imputing missing data as median

#### Model development
- Using TPOT to identify best model and hyperparameters
- Using Parfit to perform Grid Search
- Training a random forest with hyperparameters identified above

#### Quantifying performance
- Assessing accuracy, AUC, F1 score and plotting confusion matrix
- Calculating gini importances
- Plotting precision-recall curve


## Findings (Brief Summary):
Calculating the Gini Importances for the features demonstrated a good spread across the top 30 variables. The most strongly predictive variables are those related to recoveries, late fees, total loan amount and interest rate and grade, all of which make intuitive sense.




