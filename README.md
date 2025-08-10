# Logistic Regression Model Evaluation

This project demonstrates how to train and evaluate a **Logistic Regression** classifier using a breast cancer diagnosis dataset (`data.csv`). It includes steps for preprocessing, training, performance evaluation, and visualization.

---

## **Dataset**

* The dataset is expected to be a **Breast Cancer Wisconsin dataset** (from Kaggle or UCI).
* Columns:

  * `id` and `Unnamed: 32` are dropped as they are not useful.
  * `diagnosis` is mapped to:

    * `M` = 1 (Malignant)
    * `B` = 0 (Benign)

---

## **Workflow**

### **1. Data Preprocessing**

* Remove unused columns.
* Encode categorical target variable.
* Split into **train** and **test** sets.
* Standardize features using `StandardScaler`.

### **2. Model Training**

* Use `LogisticRegression` from `scikit-learn`.
* Fit the model with the training data.

### **3. Predictions**

* Predict probabilities using `model.predict_proba()`.
* Generate class predictions at both default and custom thresholds.

### **4. Metrics**

* **Confusion Matrix**
* **Precision, Recall, F1-Score**
* **ROC-AUC Score**
* **Classification Report**

### **5. Threshold Optimization**

* Compute **Precision-Recall curve**.
* Find the threshold that maximizes **F1-score**.
* Evaluate metrics at the best threshold.

### **6. Visualization**

* **ROC Curve** with AUC value.
* **Precision-Recall Curve** with best threshold marked.

---

## **Key Functions Used**

| Function                   | Purpose                                         |
| -------------------------- | ----------------------------------------------- |
| `train_test_split()`       | Split dataset into training and testing subsets |
| `StandardScaler()`         | Standardize features                            |
| `LogisticRegression()`     | Train logistic regression model                 |
| `roc_auc_score()`          | Calculate area under ROC curve                  |
| `precision_recall_curve()` | Get precision-recall pairs for thresholds       |
| `roc_curve()`              | Get TPR and FPR for ROC plot                    |

---

## How to Run

1. Place `data.csv` in the same directory as `Task-4.ipynb`.
2. Run all cells in the notebook.
3. Check printed metrics and plots.

---

## **Example Output**

```
Best threshold by F1 score: 0.4848
Best F1 score: 0.9767

Confusion Matrix:
 [[70  1]
 [ 1 42]]
ROC AUC Score: 0.9974
Precision: 0.9767
Recall: 0.9767
F1 Score: 0.9767
```

---

## Author

Jenish Allen Immanuel J 💙
