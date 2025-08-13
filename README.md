# Banking institution marketing campaigns
This practical assignment 3 that is to analyze Banking institution marketing campaigns data.

Project Overview
This notebook compares the performance of 4 classification algorithms
- K Nearest Neighbor
- Logistic Regression
- Decision Trees
- Support Vector Machines
on a bank marketing dataset. The goal is to predict whether a client will subscribe to a term deposit based on various features.

Data Source
The dataset is from the UCI Machine Learning repository: https://archive.ics.uci.edu/ml/datasets/bank+marketing
More information about the data and features can be found in the accompanying paper: CRISP-DM-BANK.pdf

Data Understanding
The dataset contains quite a lot of information about bank clients and their interactions with marketing campaigns. The target variable is 'y', indicating whether the client subscribed to a term deposit ('yes' or 'no').

Features include:
Bank client data -> age, job, marital, education, default, housing, loan
Also contains related information around last contact of the current campaign (contact, month, day_of_week, duration)
Other attributes (campaign, pdays, previous, poutcome)
Social and economic context attributes (emp.var.rate, cons.price.idx, cons.conf.idx, euribor3m, nr.employed)
Initial data cleaning involved removing rows with 'unknown' values in 'default', 'housing', and 'loan' columns, and dropping features not considered relevant for the analysis.

Feature Engineering
Categorical features were one-hot encoded, and numerical features were scaled using StandardScaler.

Modeling
The following classification models were trained and evaluated:
- K Nearest Neighbor
- Logistic Regression
- Decision Tree
- Support Vector Machine
A baseline model using DummyClassifier was established for comparison purposes.

Hyperparameter tuning was performed using GridSearchCV for each model to improve performance.

Results
The performance of each model was evaluated based on accuracy. Both initial results and results after hyperparameter tuning are presented and compared.
The comparison of initial and tuned model performance showed that hyperparameter tuning improved the accuracy of the K Nearest Neighbors and Decision Tree models, while the Logistic Regression and SVM models maintained their initial accuracy.
