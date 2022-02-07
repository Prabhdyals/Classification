## Background

Mortgages, student and auto loans, and debt consolidation are just a few examples of credit and loans that people seek online. Peer-to-peer lending services such as Loans Canada and Mogo let investors loan people money without using a bank. However, because investors always want to mitigate risk, a client has asked that you help them predict credit risk with machine learning techniques.

Built and evaluated several machine learning models to predict credit risk using data typically seen from peer-to-peer lending services. Credit risk is an inherently imbalanced classification problem (the number of good loans is much larger than the number of at-risk loans), so you will need to employ different techniques for training and evaluating models with imbalanced classes. Use the imbalanced-learn and Scikit-learn libraries to build and evaluate models using the two following techniques:

1. [Resampling](#Resampling)
2. [Ensemble Learning](#Ensemble-Learning)

- - -

## Files

[Resampling Notebook](Starter_Code/credit_risk_resampling.ipynb)

[Ensemble Notebook](Starter_Code/credit_risk_ensemble.ipynb)

[Lending Club Loans Data](Resources/LoanStats_2019Q1.csv.zip)

### Resampling

Used the [imbalanced learn](https://imbalanced-learn.readthedocs.io) library to resample the LendingClub data and built and evaluated logistic regression classifiers using the resampled data.

1. Read the CSV into a DataFrame.

2. Split the data into Training and Testing sets.

3. Scaled the training and testing data using the `StandardScaler` from `sklearn.preprocessing`.

4. Solved for Simple Logistic Regression:
    * Fitted the `logistic regression classifier`.
    * Calculated the `balanced accuracy score`.
    * Displayed the `confusion matrix`.
    * Printed the `imbalanced classification report`.

5. Oversampled the data using the `Naive Random Oversampler` and `SMOTE` algorithms.

6. Undersampled the data using the `Cluster Centroids` algorithm.

7. Over- and undersample using a combination `SMOTEENN` algorithm.

8. For each of the above:

 a. Trained a `logistic regression classifier` from `sklearn.linear_model` using the resampled data.

 b. Calculated the `balanced accuracy score` from `sklearn.metrics`.

 c. Displayed the `confusion matrix` from `sklearn.metrics`.

 d. Printed the `imbalanced classification report` from `imblearn.metrics`.

### Ensemble Learning

In this section, trained and compared two different ensemble classifiers to predict loan risk and evaluate each model. used the [Balanced Random Forest Classifier](https://imbalanced-learn.org/stable/references/generated/imblearn.ensemble.BalancedRandomForestClassifier.html) and the [Easy Ensemble Classifier](https://imbalanced-learn.org/stable/references/generated/imblearn.ensemble.EasyEnsembleClassifier.html). 

1. Read the data into a DataFrame using the provided starter code.

2. Split the data into training and testing sets.

3. Scaled the training and testing data using the `StandardScaler` from `sklearn.preprocessing`.

Then, completed the following steps for each model:

1. Trained the modeled using the quarterly data from LendingClub provided in the `Resource` folder.

2. Calculate the balanced accuracy score from `sklearn.metrics`.

3. Displayed the confusion matrix from `sklearn.metrics`.

4. Generated a classification report using the `imbalanced_classification_report` from imbalanced learn.

5. For the balanced random forest classifier only, printed the feature importance sorted in descending order (most important feature to least important) along with the feature score.
