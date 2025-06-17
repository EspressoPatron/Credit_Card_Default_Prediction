# Credit Card Behaviour Score Prediction
![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Model](https://img.shields.io/badge/Focus-F2--Score%20Optimization-blueviolet)

> Predicting next-month default risk using financial behavioral features, threshold tuning, and ensemble learning.

---

## Overview

This project aims to build a forward-looking behavioural score model to predict whether
a credit card customer will default in the upcoming billing cycle. We applied advanced
data preprocessing, financial feature engineering, and supervised classification models. The
model is evaluated using F2-score, AUC-ROC, and threshold tuning strategies that align
with real-world risk tolerance.

The pipeline includes:
-  Financial domain-specific feature engineering
-  SMOTE-based resampling to fix class imbalance
-  Threshold tuning to align predictions with credit risk priorities
-  Ensemble modeling using Voting and Stacking classifiers

---

## Techniques Used

- **Univariate & Bivariate EDA** to discover trends
- **Behavioral Feature Engineering**:
  - Credit Utilization Ratio
  - Repayment Consistency (mean, std)
  - Delinquency Streaks
  - Bill & Payment Slopes
  - Overpayment / High Utilization Flags
- **SMOTE** to handle class imbalance
- **Model Training**:
  - Logistic Regression
  - Decision Tree
  - Random Forest
  - XGBoost
  - LightGBM
  - Ensemble: Voting & Stacking Classifiers
- **Threshold Optimization** for F2-score maximization

---

## Model Performance

Several evaluation metrics were considered during model development, including Accuracy, Pre-
cision, Recall, F1-score, F2-score, and ROC-AUC. However, after reviewing the business context
and implications of misclassification, the F2-score was prioritized as the primary model selection
criterion.

The Best Model recommended was: Tuned LightGBM at 0.30 threshold, getting F2 score of 0.57 and accuracy of 0.78

![PHOTO-2025-06-17-11-54-56](https://github.com/user-attachments/assets/ee739ee2-d2db-4216-b6f3-5c841d18cd37)


---

## Conclusion

Our best model predicted 27.01% as defaulters which is greater than the actual defaulters (19.04%)
train dataset had (real world). This model provides a risk-sensitive, interpretable scoring system
that supports Bank A’s early-warning strategy. By combining robust EDA, financial engineering,
and tuned classification pipelines, the solution aligns technical accuracy with business impact.

