# Problem Statement
A telecommunications company provides subscription-based services including mobile phone connectivity, internet access, and digital entertainment services such as streaming television and movies. Revenue is primarily generated through recurring customer subscriptions, with customers billed monthly or annually depending on their contract type and payment arrangement. As with most subscription-based businesses, long-term profitability depends heavily on retaining existing customers rather than continuously acquiring new ones.

In this context, customer churn refers to customers who discontinue their relationship with the company. Within the provided dataset, churn is explicitly captured as a binary target variable (Churn), where a value of “Yes” indicates that a customer has left the service and “No” indicates that the customer remains active. This framing positions churn prediction as a supervised classification problem, where historical customer data is used to learn patterns associated with customer attrition.
Churn is a critical business concern because acquiring new customers is significantly more expensive than retaining existing ones. When a customer churns, the company not only loses future subscription revenue but may also incur additional marketing and promotional costs to replace that customer. Early identification of customers who are at risk of churning allows the business to intervene proactively through targeted retention strategies such as contract adjustments, service improvements, or personalized incentives.

The objective of this analysis is to develop a predictive model that estimates the likelihood of customer churn based on demographic attributes, service usage patterns, contract details, and billing information. By leveraging these features, the model aims to identify high-risk customers early enough for the business to take preventive action, thereby reducing churn rates and protecting long-term revenue.


## Modeling
Logistic Regression (baseline, interpretable) is the classification models that was trained and evaluated

## Evaluation metrics:

Precision, Recall, F1-score
Confusion Matrix
ROC-AUC
5. Postdictive Analysis
Analyzed false negatives (missed churners) and false positives
Identified where the model performs well and where it fails
Highlighted data limitations and unobserved churn drivers

## Business Interpretation

The model identifies most churners (high recall = 79%), so it’s useful for retention campaigns.

Some false positives (precision = 50%) → not all predicted churners will actually churn. That’s acceptable if retention incentives are cheap.

Non-churners are sometimes predicted as churners (FP = 298) → might result in unnecessary marketing spend.

## Observation:

High recall for churners (Yes = 0.79) → model is good at catching churners, which is what we care about in business.

Precision for churners is lower (0.50) → half of predicted churners are false alarms → may cost some unnecessary retention campaigns.

### Tools
Python
Pandas, NumPy
Scikit-learn
Jupyter Notebook
