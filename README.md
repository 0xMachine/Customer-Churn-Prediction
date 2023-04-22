# Customer-Churn-Prediction
This repository contains code for predicting customer churn using XGBoost. The goal of this project is to identify customers who are at risk of leaving the company, so that the company can take steps to retain them.

# Data
The dataset used in this project was created using synthetic data. It contains information about customers' demographics, usage behavior, and customer service interactions. The dataset has the following columns:

customer_id: The ID of the customer.

age: The age of the customer.

gender: The gender of the customer.

location: The location of the customer (urban, suburban, or rural).

income: The income of the customer.

credit_score: The credit score of the customer.

monthly_usage: The amount of data used by the customer per month.

average_session_time: The average length of the customer's data sessions.

num_sessions_per_month: The number of data sessions the customer has per month.

customer_service_calls: The number of customer service calls the customer has made.

churn: Whether or not the customer has churned (1 for churned, 0 for not churned).

# Model 
The model used to predict churn is an XGBoost classifier. The data is resampled using the RandomOverSampler algorithm to address class imbalance, and the model is tuned using GridSearchCV to find the best hyperparameters. The following hyperparameters were tuned:

learning_rate: The learning rate of the XGBoost model.

max_depth: The maximum depth of each decision tree in the XGBoost model.

n_estimators: The number of decision trees in the XGBoost model.

scale_pos_weight: The weight given to the positive class in the XGBoost model.

The model is evaluated on the F1 score, as this metric is better suited to imbalanced datasets than accuracy.

# Results
The XGBoost model achieved an F1 score of 0.179 on the test set. The classification report shows that the model has high recall for the positive class (churned customers), but low precision. This means that the model is good at identifying customers who are at risk of churning, but it also generates a large number of false positives. Further work could be done to improve the precision of the model, perhaps by collecting additional data or trying different resampling techniques.

# Usage
To run the code in this repository, you will need to have Python 3 and the following packages installed:

pandas

numpy

scikit-learn

xgboost

imbalanced-learn

Once you have installed these packages, you can run the main.py script to train and evaluate the model. The script will output the classification report and the F1 score on the test set.

