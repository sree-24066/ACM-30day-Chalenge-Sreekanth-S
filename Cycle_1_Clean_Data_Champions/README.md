#  Cycle 1: Clean Data Champions

##  Progress Tracker

| Day | Task Name               | Status        |
|-----|-------------------------|---------------|
| 1   | Burnout Breakdown       | ✅ Completed  |
| 2   | Stress Signals          | ✅ Completed  |
| 3   | Outlier Overload        | ⏳ Upcoming   |
| 4   | Encode to Survive       | ⏳ Upcoming   |
| 5   | Prepping for Prediction | ⏳ Upcoming   |
| -   | Mini Challenge          | ⏳ Upcoming   |
| -   | Main Challenge          | ⏳ Upcoming   |

---

##  Cycle Overview

In this cycle, I worked on a real-world mental health and burnout dataset to learn and apply preprocessing and regression techniques.

**Skills practiced:**
- Handling missing values with median/mode
- Encoding categorical variables (One-Hot)
- Scaling (Min-Max) and normalization (Box-Cox)
- Feature selection using mutual information
- Regression modeling and evaluation with MSE and R²

---

##  Daily Summaries

###  Day 1 – Burnout Breakdown
- Checked for null values
- Handled missing data using median (numerical) and mode (categorical)
- Ensured dataset readiness using `info()` and descriptive stats

###  Day 2 – Stress Signals
- Encoded categorical columns using One-Hot Encoding
- Applied Min-Max Scaling and Box-Cox Normalization
- Selected top 10 features using mutual information
- Created interaction features:  
  - `StressLevel × WorkHoursPerWeek`  
  - `SleepHours × StressLevel`
- Trained 3 regression models (Linear, Ridge, Lasso)
- ✅ **Best model:** Lasso Regression

**Model Evaluation Metrics:**

| Model            | MSE     | R² Score |
|------------------|---------|----------|
| Linear Regression| 1.0395  | -0.0637  |
| Ridge Regression | 1.0392  | -0.0634  |
| Lasso Regression | 0.9796  | -0.0024  |

---

##  Tools & Libraries

- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `sklearn.preprocessing` – MinMaxScaler, LabelEncoder
- `mlxtend`, `scipy.stats` – Box-Cox normalization
- `sklearn.linear_model` – Linear, Ridge, Lasso Regression
- `sklearn.metrics` – MSE, R² Score
- `sklearn.feature_selection` – mutual_info_regression

---

>  **Notebook Files Available Inside:**  
[`Day_01_Burnout_Breakdown.ipynb`](./Day_01_Burnout_Breakdown.ipynb)  
[`Day_02_Stress_Signals.ipynb`](./Day_02_Stress_Signals.ipynb)
