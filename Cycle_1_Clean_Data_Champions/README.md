# Cycle 1: Clean Data Champions

## Progress Tracker

| Day | Task Name                  | Status        |
|-----|----------------------------|----------------|
| 1   | Burnout Breakdown          | ✅ Completed   |
| 2   | Feature Forge + Regression | ✅ Completed   |
| 3   | Classifier Arena           | ✅ Completed   |
---
---

##  Cycle Overview

In this cycle, I worked on a real-world mental health and burnout dataset to learn and apply data cleaning, preprocessing, regression, and classification techniques.

###  Skills Practiced:
- Handling missing values using median/mode  
- Encoding categorical variables (One-Hot Encoding)  
- Feature scaling (Min-Max) and normalization (Box-Cox)  
- Feature selection using Mutual Information  
- Interaction feature creation  
- Regression modeling (Linear, Ridge, Lasso)  
- Classification modeling (Logistic Regression, LDA)  
- Evaluation using MSE, R², Accuracy, Confusion Matrix, ROC-AUC  

---

##  Daily Summaries

###  Day 1 – Burnout Breakdown
- Checked for missing/null values  
- Imputed missing values:
  - **Median** for numeric  
  - **Mode** for categorical  
- Verified data readiness using `df.info()` and descriptive stats  

---

###  Day 2 – Feature Forge + Regression
- One-Hot Encoded categorical columns  
- Applied Min-Max Scaling and Box-Cox Normalization to numerical features  
- Selected top 10 features using Mutual Information  
- Created interaction features:
  - `StressLevel × WorkHoursPerWeek`  
  - `SleepHours × StressLevel`  
- Trained 3 regression models:
  - Linear Regression  
  - Ridge Regression  
  - Lasso Regression  

✅ **Best model:** Lasso Regression (lowest MSE)

####  Regression Model Evaluation

| Model             | MSE     | R² Score |
|------------------|---------|----------|
| Linear Regression| 1.0395  | -0.0637  |
| Ridge Regression | 1.0392  | -0.0634  |
| Lasso Regression | 0.9796  | -0.0024  |

---

###  Day 3 – Classifier Arena
- Built binary classifiers to predict **BurnoutRisk (0/1)**  
- Trained:
  - Logistic Regression  
  - Linear Discriminant Analysis (LDA)  
- Evaluated using:
  - Accuracy  
  - Confusion Matrix  
  - ROC-AUC with ROC Curve Plot  

✅ **Best model:** LDA (slightly higher ROC-AUC)

####  Classification Model Evaluation

| Model              | Accuracy | ROC-AUC |
|-------------------|----------|---------|
| Logistic Regression | 88.17%   | 0.8490  |
| LDA                | 88.17%   | 0.8499  |

---

## Tools & Libraries

- `pandas`, `numpy`, `matplotlib`, `seaborn`  
- `scikit-learn` (`preprocessing`, `linear_model`, `metrics`, `discriminant_analysis`)  
- `mlxtend`, `scipy.stats` (for Box-Cox and minmax scaling)  

---

##  Notebook Files Inside

- `Day_01_Burnout_Breakdown.ipynb`  
- `Day_02_Stress_Signals.ipynb`  
- `Day_03_Classifier_Arena.ipynb`  
