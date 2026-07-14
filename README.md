## Hospital Readmission Prediction Using Machine Learning

### Overview

Hospital readmissions are a major challenge for healthcare providers, leading to increased medical costs and reduced quality of patient care. Early identification of patients at high risk of readmission enables hospitals to provide timely interventions and improve patient outcomes.

This project develops an end-to-end machine learning pipeline to predict hospital readmissions using the **Diabetes 130-US Hospitals (1999–2008)** dataset from the **UCI Machine Learning Repository**. The project covers the complete machine learning workflow, including data cleaning, feature engineering, exploratory data analysis, preprocessing, feature selection, model development, hyperparameter tuning, and performance evaluation.

---

### Dataset

**Source:** UCI Machine Learning Repository

**Dataset:** Diabetes 130-US Hospitals for Years 1999–2008

#### Dataset Summary

- **101,766** hospital encounters
- **50** original features
- **3-class classification problem**
  - Readmitted within 30 days (`<30`)
  - Readmitted after 30 days (`>30`)
  - No readmission (`NO`)

---

### Project Workflow

```
Dataset Collection
        │
        ▼
Data Understanding
        │
        ▼
Data Cleaning
        │
        ▼
Feature Engineering
        │
        ▼
Feature Reduction
        │
        ▼
Exploratory Data Analysis
        │
        ▼
Preprocessing Strategy
        │
        ▼
Train-Test Split
        │
        ▼
Preprocessing Pipeline
        │
        ▼
Feature Selection
        │
        ▼
Model Development
        │
        ▼
Hyperparameter Optimisation
        │
        ▼
Cross Validation
        │
        ▼
Model Evaluation
        │
        ▼
Model Comparison
        │
        ▼
Final Model
```

---

## Features Implemented

### Data Cleaning

- Removed unnecessary identifier columns
- Handled missing values
- Removed near-zero variance medication features
- Removed clinically uninformative features

---

### Feature Engineering

Several domain-specific feature engineering techniques were applied, including:

- Age range conversion to midpoint values
- ICD-9 diagnosis grouping
- Admission type grouping
- Discharge disposition grouping
- Admission source grouping
- Medical specialty grouping

---

### Exploratory Data Analysis

Performed detailed exploratory analysis including:

- Dataset overview
- Missing value analysis
- Class distribution
- Descriptive statistics
- Distribution analysis
- Outlier analysis
- Correlation analysis
- Medication category analysis

---

### Data Preprocessing

A reusable preprocessing pipeline was built using Scikit-learn.

#### Categorical Features

- Binary Encoding
- One-Hot Encoding

#### Numerical Features

- StandardScaler

The preprocessing pipeline was implemented using:

- ColumnTransformer
- Pipeline

to ensure **no data leakage** during model training.

---

### Feature Selection

Feature importance was evaluated using multiple approaches.

#### Filter Methods

- Chi-Square
- Mutual Information

#### Embedded Method

- Random Forest Feature Importance

The selected features were then used for model training.

---

### Machine Learning Models

The following supervised learning models were developed and compared:

- Logistic Regression
- Decision Tree
- Random Forest

Each model was trained using:

- Baseline configuration
- Hyperparameter optimisation
- Stratified Cross Validation

---

### Evaluation Metrics

Model performance was evaluated using multiple classification metrics.

- Accuracy
- Precision
- Recall
- F1-score
- Classification Report
- Confusion Matrix

Using multiple evaluation metrics provides a more reliable assessment than relying on accuracy alone, particularly for imbalanced healthcare datasets.

---

### Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---

### Skills Demonstrated

This project demonstrates practical experience in:

- Exploratory Data Analysis (EDA)
- Data Cleaning
- Feature Engineering
- Data Preprocessing
- Machine Learning Pipelines
- Feature Selection
- Hyperparameter Optimisation
- Cross Validation
- Classification Model Evaluation
- Healthcare Data Analytics

---
