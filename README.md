Customer Churn Prediction in Telecommunications

Project Overview

SyriaTel, a telecommunications provider, faces significant challenges with customer churn. High churn rates negatively impact revenue, growth, and customer loyalty. This project aims to:

Identify the key drivers of churn and

Build predictive models to mitigate churn, enabling SyriaTel to enhance customer retention strategies and improve business performance.

Business Problem

Problem Statement: High customer churn impacts revenue and loyalty.

Objective: Identify at-risk customers and key churn drivers to develop targeted retention strategies.

Project Objectives

Understand Key Drivers of Customer Churn: Analyze customer data to identify critical features that contribute to churn behavior.

Build an Accurate Predictive Model: Develop machine learning models to classify customers at risk of churning.

Offer Strategic Recommendations: Provide actionable insights to reduce churn and enhance customer loyalty.

Dataset Description

Source: SyriaTel Customer Churn Dataset

Size: 3333 rows, 21 columns

Features: Customer account details, usage statistics, and subscription plans

Goal: Predict churn based on features

Data Preparation

1. Splitting Data

The dataset is split into training and testing sets to ensure the model is trained and evaluated properly.

2. Encoding Categorical Variables

Categorical features (e.g., voice mail plan, international plan) are encoded into numeric values for model compatibility.

3. Dropping Irrelevant and Highly Correlated Features

Columns like area code and total charge features were dropped due to irrelevance and high correlation (above 0.85), preventing multicollinearity.

4. Feature Scaling

StandardScaler was applied to ensure numerical features are on the same scale.

Objective 1: Key Drivers of Customer Churn

Method: Random Forest Classifier was used to identify feature importance. The top features were:

Total Day Minutes: Lower usage correlates with higher churn risk.

Customer Service Calls: Higher calls indicate potential dissatisfaction.

Insights:

Customers with low usage may benefit from personalized plans to increase engagement.

High service interactions suggest a need for improved support.

Objective 2: Building a Predictive Model

Model Used: Random Forest Classifier

2.1 Model Evaluation

Accuracy: 90.25%

Metrics: Classification Report and Confusion Matrix were used to evaluate precision, recall, and F1-score.

2.2 Cross-Validation

Method: 5-Fold Cross-Validation

Mean Accuracy: 91.26%, indicating good model generalization.

2.3 Threshold Adjustment

Tested thresholds (0.3, 0.4, 0.5, 0.6, 0.7) to balance precision and recall.

Lower thresholds improve recall but increase false positives.

2.4 Model Comparison

Random Forest Accuracy: 90.25%

Decision Tree Accuracy: 86.00%

Reason for Selection: Random Forest outperformed Decision Tree in accuracy and class imbalance handling.

Objective 3: Strategic Recommendations

3.1 High-Risk Customer Retention

Identified 20 customers at high risk (>90% churn probability).

Recommendation: Implement personalized loyalty rewards and improve service quality for these customers.

3.2 Personalized Offers

Identified low engagement customers (e.g., those with low Total Day Minutes).

Recommendation: Offer incentives to increase engagement, such as discounts or customized plans.

3.3 Enhancing Customer Support

Customers with frequent service calls correlate with churn risk.

Recommendation: Address issues proactively and consider VIP support options.

Model Saving

The trained Random Forest model was saved as random_forest_model.pkl for future use.

Conclusion

This project successfully identified key churn drivers and built a predictive model with high accuracy. By implementing strategic recommendations, SyriaTel can significantly reduce churn and improve customer retention.

Future Improvements

Include additional features such as customer satisfaction scores.

Experiment with advanced models like Gradient Boosting.

Regularly update the model with new customer data for better performance.

