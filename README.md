CUSTOMER CHURN CLASSIFICATION PROJECT
==============================
📖 OVERVIEW
==============================

This project focuses on predicting customer churn using machine learning classification techniques.

The main objective is to build a model that can identify customers who are likely to stop using a service so that the business can take proactive retention actions.

The workflow includes:

Business understanding
Data understanding
Data preparation
Model building
Model evaluation
Business recommendations
==============================
🎯 BUSINESS PROBLEM
==============================

The business is experiencing customer loss (churn), which reduces revenue and long-term growth.

Problem Statement:

How can we predict customers who are likely to churn so that the business can intervene early and improve retention?

==============================
👥 STAKEHOLDERS
==============================
Customer Retention Team → identifies at-risk customers
Marketing Team → targets customers with retention campaigns
Business Management → reduces revenue loss
Customer Support Team → improves customer experience
==============================
📊 DATA UNDERSTANDING
==============================

The dataset contains customer behavioral and account information.

Key features include:
Account length
Service usage (calls, minutes, charges)
International plan
Voice mail plan
Customer service calls
Geographic data (state)
Target variable: churn
Dataset properties:
3333 rows
21 original features
Binary target variable (churn: yes/no)
Key insight:

The dataset is imbalanced:

~85% non-churn customers
~15% churn customers

This makes recall a more important metric than accuracy.

==============================
🧹 DATA PREPARATION
==============================

The following preprocessing steps were applied:

1. Target encoding
Converted churn to binary values (0 and 1)
2. Feature encoding
Converted:
international plan → 0/1
voice mail plan → 0/1
3. One-hot encoding
Converted state column into dummy variables
4. Feature selection
Removed irrelevant identifiers (e.g. phone number if present)
5. Missing values
Checked and handled missing values
6. Train-test split
80% training data
20% testing data
Stratified to preserve class balance
7. Feature scaling
Applied StandardScaler for Logistic Regression
Prevented data leakage by fitting only on training data
==============================
🤖 MODELING
==============================

Three classification models were built:

1. Logistic Regression (Baseline Model)
Simple and interpretable
Used as performance benchmark
Requires scaled features
2. Decision Tree Classifier
Captures non-linear relationships
Does not require scaling
More flexible than logistic regression
3. Tuned Decision Tree
Improved using hyperparameters:
max_depth
min_samples_split
Reduced overfitting
Improved generalization
==============================
📏 MODEL EVALUATION
==============================

Models were evaluated using:

Recall (Primary Metric)
Precision
F1 Score
Accuracy (Secondary Metric)
Why Recall?

In churn prediction, failing to identify a churner (false negative) is more costly than incorrectly predicting churn.

=============================
🏆 RESULTS
==============================
Logistic Regression: Baseline performance
Decision Tree: Improved non-linear learning
Tuned Decision Tree: Best overall performance
Final selected model:

👉 Tuned Decision Tree (based on Recall performance)

==============================
📊 FEATURE INSIGHTS
==============================

Most important features influencing churn:

Customer service calls
International plan
Usage patterns (day/evening/night charges)
Total call minutes

These features help explain customer churn behavior.

==============================
⚠️ LIMITATIONS
==============================
Class imbalance affects prediction performance
Limited external behavioral data
Some churn cases are still misclassified
Model performance depends on dataset quality
==============================
💡 BUSINESS RECOMMENDATIONS
==============================
Target customers with high customer service interactions
Monitor international plan users closely
Provide retention offers to high-risk customers
Improve customer support experience
Use model predictions for proactive retention strategies
