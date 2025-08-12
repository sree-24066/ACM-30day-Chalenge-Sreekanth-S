# Final Cycle

## Progress Tracker
| Day | Task Name | Status |
|-----|-----------|--------|
| 1 | Phase 1: Workout Dropout Prediction (MLP) | ✅ Completed |
| 2 | Phase 2: Workout Style Clustering (k-Means + PCA) | ✅ Completed |

---

## Cycle Overview
This final cycle focused on applying both **supervised** and **unsupervised** machine learning techniques to a fitness dataset.  
The first phase used **deep learning (MLP)** for binary classification to predict user workout dropout tendencies based on engagement survey data.  
The second phase explored **clustering** to segment workout styles using PCA for dimensionality reduction and silhouette score evaluation.  
Together, these phases showcased end-to-end predictive modeling and pattern discovery in behavioral datasets.

---

## Skills Practiced
- **Supervised Learning**: Multi-Layer Perceptron (PyTorch)  
- **Unsupervised Learning**: k-Means Clustering  
- **Dimensionality Reduction**: Principal Component Analysis (PCA)  
- **Evaluation Metrics**: Precision, Recall, F1-score, Accuracy, Silhouette Score  
- **Data Preprocessing**: Encoding categorical variables, scaling, handling missing values  
- **Feature Engineering**: Mood mapping, intensity encoding, one-hot encoding  
- **Visualization**: Matplotlib, Seaborn scatterplots for PCA projections  
- **Tools**: pandas, numpy, scikit-learn, PyTorch  

---

## Phase Summaries

### Phase 1 – Workout Dropout Prediction (MLP)
- **Dataset**: HR Engagement Survey with workout-related behavioral attributes  
- Steps:
  1. Loaded and explored dataset (checked structure, missing values)  
  2. Cleaned data (mapped `Status` to binary, encoded categorical features, scaled numeric features)  
  3. Converted processed features and labels into **PyTorch tensors**  
  4. Created **DataLoader** objects for training and validation  
  5. Defined a **Multi-Layer Perceptron**:
     - Input layer → 64 → 32 → Output (Sigmoid)
  6. Trained using **BCELoss** and **Adam optimizer** for 10 epochs  
  7. Evaluated model performance using **Precision, Recall, and F1-score**  
- **Insight**: The MLP effectively learned patterns in engagement data, with balanced precision and recall—indicating suitability for dropout risk prediction.

---

### Phase 2 – Workout Style Clustering (k-Means + PCA)
- **Dataset**: Workout fitness tracker data with demographics, workout type, intensity, and mood changes  
- Steps:
  1. Dropped irrelevant identifiers (`User ID`)  
  2. Encoded categorical features (Gender, Workout Type → one-hot; Workout Intensity → label encoding)  
  3. Mapped mood before and after workouts into numerical scores  
  4. Scaled all features using **StandardScaler**  
  5. Applied **PCA** to reduce to 2 components for visualization  
  6. Ran **k-Means clustering** with k=3 (Active, Lazy, Inconsistent groups)  
  7. Calculated **Silhouette Score** to assess cluster quality  
  8. Visualized clusters in PCA space with Seaborn scatterplot  
- **Insight**: PCA visualization showed well-separated Active and Lazy clusters, while Inconsistent styles overlapped partially, reflecting real-world workout habit diversity.

---

## Notebook Files Inside
- `Phase1__WorkoutDropoutPrediction(MLP).ipynb`  
- `Phase2__WorkoutStyleClustering.ipynb`  

---

## Tools Used
- **Libraries**: pandas, numpy, seaborn, matplotlib, scikit-learn, PyTorch  
- **ML Models**: MLP Classifier (PyTorch), k-Means Clustering  
- **Data Processing**: Label Encoding, One-Hot Encoding, Scaling, Mapping categorical to numeric  
- **Dimensionality Reduction**: PCA  
- **Metrics**: Precision, Recall, F1-score, Accuracy, Silhouette Score  

---

## Conclusion
This final cycle combined predictive modeling and clustering to address both **forecasting individual behavior** (dropout risk) and **segmenting workout patterns** in fitness datasets.  
The MLP provided actionable predictions for retention strategies, while clustering revealed behavioral groupings for targeted engagement.  
The project solidified skills in **PyTorch-based neural networks**, **unsupervised learning**, and **data preprocessing pipelines**.
