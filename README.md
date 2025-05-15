# Customer-Churn-Prediction-and-Segmentation


# Project Overview

The goal is to analyze customer churn for Knet-Flicks, a video streaming and internet company, using a dataset of customer account details and churn status (viewer_status: Churned or Stayed). The project involves exploratory data analysis (EDA), clustering to identify customer segments, supervised learning to predict churn, and actionable recommendations to reduce churn. The dataset includes features such as demographics (Age, Gender, Married), subscription details (Tenure in Months, Monthly Charge, subscription_type), and service usage (Internet Service, Streaming TV, Avg Monthly GB Download).
The analysis aims to uncover patterns in customer churn, identify at-risk segments, and provide data-driven strategies to improve customer retention, which is critical for Knet-Flicks to maintain its customer base and profitability.
# Methodology
The analysis is conducted in a Jupyter Notebook (Customer_churn_prediction.ipynb) using Python, following the assignment's four main tasks:

## Exploratory Data Analysis (EDA) and Data Preparation:

Load the dataset and compute summary statistics using pandas to understand distributions of features like Age, Monthly Charge, and Tenure in Months.
Handle missing values by assessing their impact (e.g., impute or drop based on relevance) and address outliers using statistical methods (e.g., IQR for Monthly Charge).
Convert categorical variables (e.g., Gender, Internet Service) into binary or dummy variables for modeling.
Normalize numerical features (e.g., Age, Total Charges) using StandardScaler to ensure consistent scales for clustering and supervised learning.
Visualize distributions with histograms and boxplots using matplotlib to identify patterns and anomalies.


## Clustering to Identify Customer Segments:

Select relevant features for clustering (e.g., Tenure in Months, Monthly Charge, Avg Monthly GB Download), excluding irrelevant ones like viewer_id with justification.
Scale the data using StandardScaler to ensure equal weighting of features.
Apply K-means clustering (chosen for its simplicity and effectiveness with continuous features) and determine the optimal number of clusters using the elbow method and silhouette score.
Analyze cluster characteristics (e.g., high vs. low tenure, streaming usage) and their churn rates.


## Supervised Learning for Churn Prediction:

Treat churn prediction as a classification problem (binary outcome: Churned or Stayed).
Split the data into training and testing sets using train_test_split (e.g., 80-20 split) to evaluate model performance.
Build two models:
Logistic Regression: A baseline model for interpretability.
Random Forest Classifier: To capture non-linear relationships and feature interactions.


Evaluate models using accuracy, precision, recall, and F1-score, focusing on F1-score due to potential class imbalance in churn data.
Identify the top 5 predictive features using feature importance (Random Forest) or coefficients (Logistic Regression), such as Tenure in Months, Monthly Charge, or Internet Service.
Mitigate overfitting by tuning hyperparameters (e.g., using cross-validation) and analyzing residuals.


## Churn Risk Analysis and Recommendations:

Identify the cluster with the highest churn rate by comparing viewer_status across clusters.
Analyze the segment’s characteristics (e.g., short tenure, high monthly charges) to understand churn drivers.
Recommend targeted actions, such as offering discounts to high-charge customers, improving internet service quality, or introducing loyalty programs for short-tenure customers.



This methodology ensures a thorough analysis of customer churn, combining EDA, unsupervised learning (clustering), supervised learning (prediction), and actionable business insights.
