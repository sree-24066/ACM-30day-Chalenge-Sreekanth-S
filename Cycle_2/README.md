#  Cycle 2:

##  Progress Tracker

| Day | Task Name                               | Status        |
|-----|------------------------------------------|----------------|
| 1   | Phase 1: Bagging and Boosting            | ✅ Completed |
| 2   | Phase 2: Support Vector Machines (SVM)   | ✅ Completed |
| 3   | Phase 3: Unsupervised Learning           | ✅ Completed |
| 4   | Phase 4: SVD + PCA                       | ✅ Completed |
| 5   | Phase 5: Model Validation & Selection    | ✅ Completed |
| —   | Main Challenge – Tweet Sentiment Analysis| ✅ Completed |

---

##  Cycle Overview

This cycle focused on strengthening core machine learning concepts on both structured and unstructured data. It covered classification using ensemble methods and SVMs, unsupervised learning via clustering, dimensionality reduction with PCA and SVD, and real-world text classification using TF-IDF. The main challenge demonstrated scalable ML applied to 1.6M tweets.

---

##  Skills Practiced

- **Ensemble Learning**: Random Forest, AdaBoost, XGBoost  
- **Support Vector Machines (SVM)** with Linear, RBF, and Polynomial kernels  
- **Unsupervised Learning**: k-Means, Hierarchical Clustering, t-SNE  
- **Dimensionality Reduction**: PCA, Truncated SVD  
- **Model Validation**: K-Fold Cross-Validation, Learning Curves  
- **Text Feature Extraction**: TF-IDF Vectorization  
- **Evaluation Metrics**: Accuracy, Precision, Recall, F1-score, Silhouette Score  
- **Concepts**: Bias-Variance Tradeoff, Overfitting, Underfitting  
- **Visualization**: Matplotlib, Seaborn  

---

##  Phase Summaries

---

###  Phase 1 – [Bagging and Boosting (Breast Cancer Dataset)](./Phase1_Bagging_and_Boosting.ipynb)

- Loaded and explored Breast Cancer dataset
- Preprocessed data (dropped ID, label-encoded target, scaled features)
- Trained three ensemble models:
  - `RandomForestClassifier`
  - `AdaBoostClassifier`
  - `XGBoostClassifier`

**Results Summary:**

| Model          | Accuracy | False Negatives | False Positives |
|----------------|----------|------------------|------------------|
| Random Forest  | 97.36%   | 3                | 0                |
| AdaBoost       | 98.24%   | 2                | 0                |
| XGBoost        | 95.61%   | 5                | 0                |

 **Insight**: AdaBoost achieved the best accuracy and minimized false negatives

---

###  Phase 2 – [Support Vector Machines (Credit Card Fraud Dataset)](./Phase2_SupportVectorMachines.ipynb)

- Used balanced dataset: 492 fraud + 492 non-fraud samples  
- Trained SVM with three kernels:
  - Linear
  - RBF
  - Polynomial

**Accuracy Comparison:**

| Kernel      | Accuracy |
|-------------|----------|
| Linear      | 0.9391   |
| RBF         | 0.9289   |
| Polynomial  | 0.8731   |

 **Insight**: Linear kernel worked best, indicating nearly linearly separable data. Polynomial kernel overfit.

---

### Phase 3 – [Unsupervised Learning (Iris Dataset)](./Phase3_Unsupervised Learning.ipynb)

- Removed labels for true unsupervised learning
- Scaled features using StandardScaler
- Applied:
  - k-Means (Elbow method used to pick k=3)
  - Hierarchical Clustering (dendrogram)
  - PCA and t-SNE for 2D visualization

 **Insight**: Setosa was distinctly clustered, while versicolor and virginica showed overlap—reflecting true label structure.

---

### Phase 4 – [SVD + PCA (20 Newsgroups Dataset)](./Phase4_SVD_PCA.ipynb)

- Loaded 20 Newsgroups dataset (11,314 documents)
- Transformed text into TF-IDF → `(11314 × 10000)`
- Applied Truncated SVD → `(11314 × 2)`
- Visualized documents in 2D and clustered using k-Means (k=20)

**Silhouette Score**: `0.3286`

**Insight**: SVD preserved structure in fewer dimensions. Clustering revealed document groupings even without labels.

---

### Phase 5 – [Model Validation & Selection](./Phase5_Model_Validation&Selection.ipynb)

- Used Random Forest on Breast Cancer dataset
- Applied 5-Fold Cross-Validation:
  - Scores: `[0.9561, 0.9649, 0.9386, 0.9649, 0.9646]`
  - Mean Accuracy: `0.9578`, Std Dev: `0.0102`
- Plotted Learning Curve

 **Insight**: Mild overfitting observed, but validation performance was stable. Learned key concepts of generalization, bias-variance, and model reliability.

---

###  Main Challenge – [Tweet Sentiment Analysis](./MainChallenge_TweetSentimentAnalysis.ipynb)

- Binary classification (positive/negative) of 1.6M tweets  
- Cleaned text (lowercase, removed punctuation, stopwords via NLTK)
- Extracted features with TF-IDF (top 5000 words)
- Trained Logistic Regression model

**Accuracy**: `77.36%`

**Confusion Matrix:**

|                | Predicted Negative | Predicted Positive |
|----------------|--------------------|--------------------|
| Actual Negative| 119,864            | 39,630             |
| Actual Positive| 32,797             | 127,709            |

**Classification Report:**

| Sentiment | Precision | Recall | F1-Score | Support   |
|-----------|-----------|--------|----------|-----------|
| Negative  | 0.79      | 0.75   | 0.77     | 159,494   |
| Positive  | 0.76      | 0.80   | 0.78     | 160,506   |

**Insight**: TF-IDF efficiently captured text features. Logistic Regression gave good balance of speed and accuracy for large-scale text data.

---

##  Notebook Files Inside

- `Phase1_Bagging_and_Boosting.ipynb`
- `Phase_2_SVM_Kernel_Comparison.ipynb`
- `Phase3_Unsupervised_Learning.ipynb`
- `Phase_4_SVD_PCA.ipynb`
- `Phase_5_Model_Validation_Selection.ipynb`
- `Main_Challenge_Tweet_Sentiment_Analysis.ipynb`

---

##  Tools Used

- **Libraries**: `pandas`, `numpy`, `matplotlib`, `seaborn`, `re`, `nltk`
- **ML Models**: `RandomForestClassifier`, `AdaBoostClassifier`, `XGBoostClassifier`, `SVC`, `LogisticRegression`
- **Text Processing**: `TfidfVectorizer`, `NLTK stopwords`
- **Clustering/DR**: `KMeans`, `PCA`, `TruncatedSVD`, `t-SNE`
- **Validation**: `KFold`, `cross_val_score`, `learning_curve`
- **Metrics**: `accuracy_score`, `confusion_matrix`, `classification_report`, `silhouette_score`
- **Data**: `20 Newsgroups`, `Breast Cancer`, `Iris`, `Credit Card Fraud`, `Tweet Dataset`

---

## Conclusion

This cycle deepened my ML expertise by exposing me to a wide range of challenges across classification, validation, dimensionality reduction, and NLP. From handling imbalanced fraud data to clustering unlabeled flowers and processing over a million tweets, I learned how to select models, evaluate them robustly, and communicate findings effectively through visualization and metrics.
