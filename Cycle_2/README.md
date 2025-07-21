# Cycle 2: 

## Progress Tracker

| Day | Task Name                         | Status        |
|-----|----------------------------------|----------------|
| 1   | Phase_1_Bagging & Boosting Models         | ✅ Completed |

---

## Daily Summaries

### Phase-1 – [Bagging and Boosting](./Phase1_ Bagging_and_Boosting.ipynb)

- Loaded and explored the **Breast Cancer dataset** from Kaggle
- Dropped `id` column and label-encoded `diagnosis` (M=1, B=0)
- Split data into training and test sets (80/20)
- Applied **StandardScaler** for feature scaling

✅ Trained and compared three models:
- `RandomForestClassifier`
- `AdaBoostClassifier`
- `XGBoostClassifier`

📊 **Results Summary:**

| Model         | Accuracy | False Negatives | False Positives |
|---------------|----------|------------------|------------------|
| Random Forest | 97.36%   | 3                | 0                |
| AdaBoost      | 98.24%   | 2                | 0                |
| XGBoost       | 95.61%   | 5                | 0                |

🧠 **Insight:**  
AdaBoost had the **best overall performance** with the **fewest false negatives**. All models avoided false positives, which is good for medical diagnosis.

---

## Files Included
- `ACM_Cycle2_Phase1_BreastCancer_Ensemble.ipynb`

---

## Tools Used

- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `scikit-learn` (RandomForest, AdaBoost, metrics)
- `xgboost`
