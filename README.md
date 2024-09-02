# Customer-churn-prediction-model--the-case-of-a-bank
This project aims to build a machine learning model to predict whether bank customers will churn or not. The churn rate - rate at which bank customers stop doing business with the bank. 

## Customer Churn Prediction Model: The Case of a Bank

## Objective

The objective of this project is to build a machine learning model that predicts whether bank customers will churn (i.e., leave the bank). By understanding the factors influencing customer churn, the bank can take proactive steps to retain customers and reduce attrition rates.

## Dataset

The dataset used in this project consists of 10,000 bank customers and includes 14 attributes such as:

	- Credit score
	- Geographical location (Germany, France, Spain)
	- Gender (male, female)
	- Age
	- Tenure (years as a bank customer)
	- Account balance
	- Estimated salary
	- Number of products purchased through the bank
	- Credit card status
	- Active member status

The dataset is imbalanced, with only 20% of customers having churned. This necessitated the use of techniques like SMOTE to balance the classes during model training.
# Methodology

## Data Preprocessing and Cleaning:
	- The dataset was cleaned by removing missing values, duplicates, and unnecessary columns.
	- Features were categorized into numerical and categorical attributes for further analysis.
## Exploratory Data Analysis (EDA):
	- Visualizations such as box plots and histograms were used to understand the distribution of numerical attributes.
	- The target variable (churn) was analyzed for distribution and imbalance.
	- The relationship between the target variable and categorical attributes was explored through count plots.
## Feature Engineering:
	- New features were created by transforming existing attributes, such as tenure relative to age, credit score categories, and balance score categories.
	- One-hot encoding was applied to categorical variables like geography and gender.
## 	Model Training:
	- The data was split into training and test sets, and SMOTE was applied to the training set to handle class imbalance.
	- Three models were trained: Random Forest with two different hyperparameter settings and LightGBM.
	- MLflow was used to track and log experiments, including model parameters and performance metrics.
## Model Evaluation:
	- The performance of each model was evaluated using metrics such as accuracy, F1 score, precision, recall, ROC AUC score, and confusion matrix.
	- The models were also saved and evaluated for future use.
## Business Intelligence:
	- The final model predictions were saved to a Delta table and visualized using Power BI to provide actionable insights for the bank.
	- Key insights included the impact of product usage, geography, age, and credit score on churn rates.
# Results

### Results from Exploratory Data Analysis (EDA)
- 1. Geographical Distribution: The majority of the bank’s customers are from France, with Spain having the lowest churn rate, indicating better customer retention in Spain compared to France and Germany.
- 2.	Credit Card Ownership: A large proportion of customers own credit cards, reflecting the widespread adoption or availability of credit card products among the bank’s clientele.
- 3.	Age and Credit Score Diversity: The customer base includes individuals over 60 years old and those with credit scores below 400. However, these characteristics do not appear as outliers, suggesting a broad range of age and credit scores among customers.
- 4.	Bank Product Usage: Most customers utilize one or two of the bank’s products, with very few using more than two. This indicates limited cross-selling opportunities or customer interest in multiple products.
- 5.	Customer Engagement and Churn: Customers who are less active in their banking activities are more likely to churn, suggesting that engagement is a critical factor in retaining customers.
- 6.	Gender and Tenure: Gender and the length of time a customer has been with the bank (tenure) do not significantly impact their likelihood of churn, indicating these factors are less critical in predicting customer attrition.


### Relationship Between Categorical Variables and Target Variable (Churn)
- 1. Geography: The churn rate varies by geographical location, with customers in Germany showing a higher likelihood of churning compared to those in France and Spain. This suggests that regional factors may influence customer retention.
- 2. Gender: The analysis indicated no significant difference in churn rates between male and female customers, implying that gender does not strongly influence the likelihood of a customer leaving the bank.
- 3. Credit Card Ownership: Customers with and without credit cards displayed similar churn rates, indicating that having a credit card does not significantly affect customer retention.
- 4. Active Member Status: Customers who are not actively engaged with the bank are more likely to churn. This highlights the importance of customer engagement in reducing attrition.
- 5. Number of Products: Customers using more than two products are more likely to churn, despite a lower overall number of such customers. This suggests that complexity or dissatisfaction with multiple products might drive some customers to leave.
- 6. Tenure: The number of years a customer has been with the bank (tenure) showed no strong correlation with churn, indicating that long-term customers are not necessarily more loyal than newer ones.

![image](https://github.com/user-attachments/assets/6d8c8427-c281-47fc-a4d3-72d92824f123)

### Insights from Business Intelligence Analysis
- 1. Churn Rate and Product Usage: Customers using more than two products have a higher churn rate, suggesting the need for further investigation into the features correlated with multi-product use.
- 2. Geographical Churn: Customers in Germany exhibited a higher churn rate than those in France and Spain, indicating a need for targeted retention strategies.
- 3. Age and Churn: Middle-aged customers (25-45) are prevalent, but churn is more frequent among customers aged 45-60.
- 4. Credit Score and Churn: Customers with lower credit scores are more likely to leave, suggesting the need for retention efforts focused on this group.
