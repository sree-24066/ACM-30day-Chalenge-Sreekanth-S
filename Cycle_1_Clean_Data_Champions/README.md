# Cycle 1: Clean Data Champions

## Progress Tracker

| Day | Task Name                       | Status        |
|-----|----------------------------------|----------------|
| 1   | Burnout Breakdown               | ✅ Completed |
| 2   | Feature Forge + Regression      | ✅ Completed |
| 3   | Classifier Arena                | ✅ Completed |
| 4   | Classifier + Feature Selection  | ✅ Completed |
| —   | Main Challenge – Dirty Dataset Detective | ✅ Completed |

---

##  Cycle Overview

This cycle focused on real-world data cleaning, feature selection, classification, and regression modeling. The final challenge was a corrupted medical insurance dataset that needed to be cleaned and modeled with R² > 0.85.

---

##  Skills Practiced

- Handling missing values (Median/Mode)
- Encoding categorical variables (One-Hot, Label Encoding)
- Feature Scaling (Min-Max, StandardScaler)
- Normalization (Box-Cox)
- Feature Selection (Mutual Information, Random Forest Importances)
- Interaction Feature Engineering
- Regression Models: Linear, Ridge, Lasso, Random Forest
- Classification Models: Logistic Regression, LDA, Decision Tree, k-NN
- Evaluation: MSE, R², Accuracy, Confusion Matrix, ROC-AUC
- Hyperparameter tuning using GridSearchCV

---

##  Daily Summaries

###  Day 1 – [Burnout Breakdown](./Day_01_Burnout_Breakdown.ipynb)
- Checked for missing/null values
- Imputed:
  - Median for numeric features
  - Mode for categorical features
- Verified data quality using `.info()` and `.describe()`

---

###  Day 2 – [Stress Signals (Feature Forge + Regression)](./Day_02_Stress_Signals.ipynb)
- One-Hot Encoded categorical variables
- Applied:
  - Min-Max Scaling
  - Box-Cox Normalization
- Selected top 10 features using Mutual Information
- Created interaction features:
  - `StressLevel × WorkHoursPerWeek`
  - `SleepHours × StressLevel`
- Trained:
  - Linear Regression
  - Ridge Regression
  - Lasso Regression

✅ **Best Model:** Lasso Regression (lowest MSE)

**Regression Model Evaluation:**

| Model              | MSE     | R² Score |
|-------------------|---------|----------|
| Linear Regression | 1.0395  | -0.0637  |
| Ridge Regression  | 1.0392  | -0.0634  |
| Lasso Regression  | 0.9796  | -0.0024  |

---

###  Day 3 – [Classifier Arena](./Day_03_Classifier_Arena.ipynb)
- Converted BurnoutRisk to binary (BurnoutBinary)
- Trained binary classifiers:
  - Logistic Regression
  - Linear Discriminant Analysis (LDA)
- Evaluated with:
  - Accuracy
  - Confusion Matrix
  - ROC-AUC

✅ **Best Model:** LDA (slightly higher ROC-AUC)

**Classification Model Evaluation:**

| Model               | Accuracy | ROC-AUC |
|--------------------|----------|---------|
| Logistic Regression| 88.17%   | 0.8490  |
| LDA                | 88.17%   | 0.8499  |

---

###  Day 4 – [Classifier + Feature Selection](./Day_04_Classifier_Feature_Selection.ipynb)
- Trained:
  - Decision Tree
  - Random Forest
  - k-NN
- Used feature importance from Random Forest to identify top 3 features:
  - `BurnoutLevel`, `ProductivityScore`, `ManagerSupportScore`
- Re-trained models using only these 3 features

**Before (All Features) vs After (3 Features) Accuracy:**

| Model         | Accuracy (Full) | Accuracy (3 Features) |
|---------------|------------------|------------------------|
| Decision Tree | ~98%             | 100%                   |
| Random Forest | ~99%             | 100%                   |
| k-NN          | ~97%             | 98%                    |

✅ **Insight:** A few strong features captured most of the prediction power.

---

##  Main Challenge – [Dirty Dataset Detective](./Main_Challenge_Dirty_Dataset_Detective.ipynb)

 Task: Clean and model the **Medical Insurance Cost Prediction** dataset (from Kaggle) with messy, inconsistent, and outlier-ridden data.

**Steps Completed:**
1. **Data Cleaning:**
   - Removed duplicates
   - Capped outliers in `bmi` and `charges` using IQR

2. **EDA:**
   - Distribution plots
   - Boxplots
   - Correlation heatmaps

3. **Feature Encoding:**
   - Label encoded `sex`, `smoker`
   - One-hot encoded `region`

4. **Feature Engineering:**
   - Created `age_smoker`, `bmi_smoker` interaction features
   - Standardized all features using `StandardScaler`

5. **Feature Selection:**
   - Used `RandomForestRegressor` to get importance scores

6. **Modeling (Baseline):**
   - Linear Regression → R² = 0.8509
   - Ridge Regression → R² = 0.8519
   - Random Forest → R² = 0.8389

7. **Hyperparameter Tuning (GridSearchCV):**
   - Tuned Random Forest → ✅ **R² = 0.8566**

8. **Visualization:**
   - Actual vs Predicted scatter plot
   - Feature importance bar chart

✅ **Final Result:** Successfully improved R² from < 0.6 to **> 0.85**

---

##  Notebook Files Inside

- `Day_01_Burnout_Breakdown.ipynb`
- `Day_02_Stress_Signals.ipynb`
- `Day_03_Classifier_Arena.ipynb`
- `Day_04_Classifier_Feature_Selection.ipynb`
- `Main_Challenge_Dirty_Dataset_Detective.ipynb`

---

##  Tools Used

- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `scikit-learn` (preprocessing, models, metrics)
- `scipy.stats`, `mlxtend`, `GridSearchCV`

---

##  Conclusion

This cycle gave me hands-on experience in real-world data cleaning, modeling, and evaluation. I explored different types of machine learning tasks—regression and classification—and learned how to engineer features and tune models effectively.

✅ **Ready for Cycle 2!**
