# Vehicle Insurance Fraud Detection
## Overview
This repository provides a comprehensive analysis of various machine learning techniques for detecting insurance fraud using vehicle insurance data. We evaluated the performance of several models—Logistic Regression, Decision Trees, Random Forests, Support Vector Machines (SVM), and Gradient Boosting—using a dataset obtained from Kaggle. The goal is to identify fraudulent claims efficiently and effectively while considering the balance between precision and recall.

## Dataset
The dataset, titled "Vehicle Insurance Fraud Detection," includes 15,421 instances of insurance claims with the following key components:
- Claim Information: Time-related details such as month, week, and day.
- Vehicle Information: Details like make, category, price, and age.
- Policy Information: Insurance policy details including type, number, deductible amount, and driver rating.
- Personal Information: Attributes such as sex, marital status, and age of the policyholder.
- Claim and Policy History: Historical data on past incidents and previous claims.
- Legal and Investigative Aspects: Legal factors like police reports, witnesses, and agent involvement.
- The target variable, FraudFound_P, indicates whether a claim is fraudulent (1) or not (0).

## Methodology
### Data Processing
- Data Collection: Dataset acquired from Kaggle.
- Data Cleaning: Outliers were identified and handled using the IQR method. No missing values were found.
- Data Transformation: Applied one-hot encoding and label encoding to convert categorical data into numerical format.
- Handling Imbalanced Data: Used SMOTE to balance the dataset and reduce bias towards the majority class.
- Data Splitting: Split data into training (80%) and testing (20%) sets.
### Models Evaluated
- Logistic Regression: High accuracy in identifying non-fraudulent claims but struggles with fraud detection.
- Decision Trees: Good for understanding patterns but has a high false positive rate for fraud cases.
- Random Forests: Offers high accuracy for non-fraudulent cases but moderate fraud detection performance.
- Support Vector Machines (SVM): Balanced precision and recall, with improved fraud detection.
- Gradient Boosting: Highest recall for fraud cases, though with a higher false positive rate.

## Results
### Model Performance
- Logistic Regression: Accuracy = 0.755, Precision (Fraud) = 0.146, Recall (Fraud) = 0.584
- Decision Tree: Accuracy = 0.858, Precision (Fraud) = 0.076, Recall (Fraud) = 0.084
- Random Forest: Accuracy = 0.894, Precision (Fraud) = 0.187, Recall (Fraud) = 0.381
- SVM: Accuracy = 0.827, Precision (Fraud) = 0.154, Recall (Fraud) = 0.381
- Gradient Boosting: Accuracy = 0.803, Precision (Fraud) = 0.242, Recall (Fraud) = 0.492
  
## Business Implications
- Logistic Regression: Useful for preliminary claim assessments but may require additional verification due to its low fraud detection precision.
- Decision Tree: Provides transparency and good non-fraud detection but needs improvement in fraud detection accuracy.
- Random Forest: Effective for screening legitimate claims but may miss some fraudulent ones.
- SVM: Offers balanced performance and improved fraud detection, though it may still produce false positives.
- Gradient Boosting: Best for detecting a high number of fraud cases but with a trade-off of increased false positives.
  
## Conclusion
Selecting the appropriate model depends on the specific needs of the insurance company. The trade-offs between precision and recall must be considered to balance fraud detection efficiency with operational costs and customer satisfaction.
