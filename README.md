
# Airline Customer Satisfaction Survey

## Introduction

In the fast-paced world of air travel, airlines strive to improve passenger experience and maintain customer loyalty. This project leverages machine learning to analyze customer feedback and predict airline passenger satisfaction based on in-flight services and passenger demographics.

We’ve built a classification model that helps airlines:
- Predict passenger satisfaction
- Identify key satisfaction drivers
- Improve service for targeted customer segments

The project uses the XGBoost algorithm due to its performance, flexibility, and ability to handle imbalanced datasets and non-linear relationships.

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Installation](#installation)
3. [Usage](#usage)
4. [Data Description](#data-description)
5. [Methodology](#methodology)
   - [Descriptive Analysis](#descriptive-analysis)
   - [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
   - [Principal Component Analysis (PCA)](#principal-component-analysis-pca)
6. [Feature Engineering](#feature-engineering)
7. [Model Building and Evaluation](#model-building-and-evaluation)
8. [Results](#results)
9. [Key Findings](#key-findings)
10. [Model Performance](#model-performance)
11. [Conclusion](#conclusion)
12. [Business Report Conclusion and Future Enhancements](#business-report-conclusion-and-future-enhancements)

---

## Project Overview

We aim to build a robust classification model that predicts whether a passenger is "Satisfied" or "Neutral/Dissatisfied" based on features such as class, type of travel, inflight services, delays, and demographics.

We experimented with models like:
- Logistic Regression
- Decision Tree
- Random Forest
- **XGBoost** (final chosen model)

---

## Installation

```bash
git clone https://github.com/hariharan-uta/airline-satisfaction-project.git
cd airline-satisfaction-project
pip install -r requirements.txt
```

---

## Usage

```bash
jupyter notebook "Airline Passenger Satisfaction Analysis Final.ipynb"
```

---

## Data Description

- **Records**: 103,904 rows
- **Attributes**:
  - Demographics: Gender, Age
  - Flight info: Flight Distance, Type of Travel, Class
  - Services: Inflight Wi-Fi, Online Boarding, Food, Seat Comfort, etc.
- **Target Variable**: `satisfaction` (Satisfied / Neutral or Dissatisfied)

---

## Methodology

### Descriptive Analysis

- Distribution of age, gender, class, and travel type.

### Exploratory Data Analysis (EDA)

We explored correlations, class imbalance, and key features.

[EDA Screenshot](c:\Users\harih\Downloads\Airline_Passenger_Satisfaction\download.png)

### Principal Component Analysis (PCA)

PCA was explored for dimensionality reduction but not used in the final model.

---

## Feature Engineering

Key steps:
- One-Hot Encoding
- Standardization
- Handling missing values
- Recursive Feature Elimination (RFE)

---

## Model Building and Evaluation

Models used:
- Logistic Regression
- Decision Tree
- Random Forest
- **XGBoost** (chosen)

---

## Results

![Satisfaction Distribution](images/satisfaction_distribution.png)
![Feature Importance](images/feature_importance_xgboost.png)

---

## Key Findings

- Business and longer travel correlates with satisfaction.
- Wi-Fi, online boarding, and seat comfort are key.

---

## Model Performance

| Model            | Accuracy | Precision | Recall | AUC  |
|------------------|----------|-----------|--------|------|
| LogisticRegression | 87%     | 0.85      | 0.86   | 0.92 |
| DecisionTree     | 95%      | 0.94      | 0.95   | 0.97 |
| RandomForest     | 95%      | 0.96      | 0.96   | 0.99 |
| **XGBoost**      | **96%**  | **0.96**  | **0.96**| **0.99** |

![ROC Curve](images/roc_curve_xgboost.png)

---

## Conclusion

XGBoost provided the best overall performance with strong accuracy, generalization, and interpretability.

---

## Business Report Conclusion and Future Enhancements

- Use insights to improve service.
- Deploy real-time models via APIs.
- Integrate feedback from reviews.
- Expand to international routes.
