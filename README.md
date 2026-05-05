# 📊 Customer Churn Prediction for Telecom Customer Retention

## 📌 Project Overview
The goal of this project is to build a machine learning classification model that predicts customer churn in a telecom company. By identifying customers who are likely to leave, the business can take proactive actions to improve retention, reduce revenue loss, and lower customer acquisition costs.



## 🎯 Business Understanding

### 1.1 Problem Statement
Customer churn is a major challenge in the telecom industry. Losing customers directly impacts revenue and increases marketing costs for acquiring new users.

### 1.2 Stakeholders
- **Customer Retention & Marketing Teams** → Target at-risk customers with promotions and retention strategies  
- **Business Analysts & Management** → Understand churn patterns and improve business strategy  

### 1.3 Objective
Build a classification model that predicts whether a customer will churn based on historical usage and account data.

### 1.4 Success Metric
- **Recall (Primary Metric)**  
We prioritize recall because failing to identify a churner is more costly than incorrectly targeting a non-churner.

### 1.5 Methodology
- Logistic Regression (Baseline model)
- Decision Tree Classifier
- Tuned Decision Tree (final model)
- Model comparison using Recall, Precision, F1-score, and Accuracy

### 1.6 Constraints
- No external business data (pricing changes, competitor behavior)
- Class imbalance (few churners compared to non-churners)



## 📂 Dataset Understanding

### Dataset Source
Telecom customer dataset containing usage patterns, service plans, and customer behavior.

### Dataset Shape
- Rows: 3333
- Columns: 21 (before preprocessing)

### Target Variable
- `churn`
  - 0 → Not churned
  - 1 → Churned

### Class Distribution
- 85% → No churn
- 15% → Churn

👉 This shows **strong class imbalance**



## 🧹 Data Preparation

### 3.1 Data Cleaning
- Removed irrelevant column: `phone number`
- Checked and handled missing values

### 3.2 Encoding
- Converted:
  - `international plan` → 0/1
  - `voice mail plan` → 0/1
  - `churn` → 0/1
- One-hot encoded `state`

### 3.3 Feature Selection
- Separated features (X) and target (y)

### 3.4 Train-Test Split
- 80% training / 20% testing
- Stratified split to preserve class balance



## 📊 Data Analysis (EDA)

### 4.1 Churn Distribution
- Majority of customers do NOT churn (~85%)
- Strong class imbalance detected

### 4.2 Customer Service Calls
- Churned customers make **more customer service calls**
- Indicates dissatisfaction and unresolved issues

### 4.3 Correlation Analysis
Top churn-related features:
- Customer service calls
- International plan
- Total day charge

👉 Insight:
Churn is influenced by **multiple factors**, not one variable



## 📈 Data Visualization

### Key Insights from Visuals

#### 1. Churn Distribution
- Highly imbalanced dataset

#### 2. Call Usage Distribution
- Most customers have moderate usage
- Some high-usage outliers exist

#### 3. Churn vs Usage
- Churned customers tend to have slightly higher usage

#### 4. Customer Service Calls vs Churn
- Strong relationship between complaints and churn

#### 5. Correlation Heatmap
- No single dominant predictor
- Moderate correlations across multiple features

---

## 🤖 Modeling

### 5.1 Models Used
- Logistic Regression (Baseline)
- Decision Tree
- Tuned Decision Tree (Final Model)


## 📌 Model Performance

| Model | Recall | Precision | F1-score | Accuracy |
|------|--------|----------|----------|----------|
| Logistic Regression | 0.27 | 0.56 | 0.36 | 0.86 |
| Decision Tree | 0.64 | 0.68 | 0.66 | 0.90 |
| Tuned Decision Tree | 0.63 | 0.76 | 0.69 | 0.92 |


## 🏆 Best Model
### Tuned Decision Tree

Why?
- Highest accuracy
- Best balance of precision and recall
- Better generalization than baseline model



## 📉 Confusion Matrix Insights

- True Negatives: 551
- False Positives: 19
- False Negatives: 36
- True Positives: 61

👉 Key focus: **Reduce False Negatives (missed churners)**


## 🔍 Feature Importance

Top predictors of churn:
- Customer service calls
- International plan
- Total day charge
- International usage
- Evening charges


## 📌 Key Business Insights

### 1. Cost drives churn
- High charges increase churn likelihood

### 2. Poor service experience
- More customer service calls → higher churn

### 3. International plan users
- More likely to churn due to higher costs

### 4. Heavy users
- High usage customers are sensitive to pricing



## ⚠️ Limitations
- Class imbalance affects model learning
- No external business factors included
- Some churn cases still misclassified



## 💡 Recommendations
- Improve customer support experience
- Offer targeted discounts for high-risk customers
- Review pricing for heavy users
- Focus retention strategies on international plan users



## ✅ Conclusion
The project successfully built a churn prediction model using machine learning. The tuned decision tree model performed best, with strong recall and accuracy, making it suitable for identifying at-risk customers and supporting business retention strategies.


###ANTONY SILA
LinkedIn: linkedin.com/in/ANTONY-SILA

https://github.com/tonny001-rgb/CUSTOMER-CHURN-CLASSIFICATION-

