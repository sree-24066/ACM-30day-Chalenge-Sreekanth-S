# Cycle 3: Redemption Cycle

## Progress Tracker

| Day | Task Name                         | Status        |
|-----|-----------------------------------|----------------|
| 1   | Phase 1: Book Dropout Predictor   | ✅ Completed |
| 2   | Phase 2: Facial Emotion Recognition (CNN)        | ⏳ Pending   |
| 3   | Phase 3: [not released]            | ⏳ Pending   |

---

##  Cycle Overview
[to be added after completing all phases]
---

##  Skills Practiced

- **Binary Classification** using a custom-built MLP in PyTorch  
- **Feature Engineering** and ethical data modeling  
- **Data Merging and Cleaning** 
- **Loss Curve Visualization** and Evaluation Metrics  
- [More to be added with other phases...]

---

##  Phase Summaries

---

### Phase 1 – [Book Dropout Predictor (Goodbooks-10K Dataset)](./Phase1_Book_Dropout.ipynb)

- Merged books.csv and ratings.csv using book_id
- Created binary label: 1 (rating ≥ 4), 0 (otherwise)
- Selected following metadata-based features:
  - average_rating
  - ratings_count
  - original_publication_year
  - books_count
- Avoided `user rating` as input to **prevent label leakage**

#### Model Architecture:
- Custom **MLP** built from scratch using PyTorch
- 2 hidden layers with ReLU activation
- Output layer with Sigmoid activation 
- Binary Cross Entropy Loss + Adam Optimizer
- Trained for 20 epochs

#### Evaluation Metrics:

| Metric     | Score   |
|------------|---------|
| Accuracy   | 66.86%  |
| Precision  | 66.86%  |
| Recall     | 100.00% |
| F1 Score   | 80.14%  |

**Insight**: High recall shows model's strength in identifying finishers. Ethical modeling with no leakage ensured fair learning.

---

##  Notebook Files Inside

- `Phase1_Book_Dropout.ipynb`


---

##  Tools Used

- **Libraries**: pandas, numpy, sklearn, matplotlib, torch
- **ML Techniques**: MLP from scratch, data normalization, label generation

---

##  Conclusion

