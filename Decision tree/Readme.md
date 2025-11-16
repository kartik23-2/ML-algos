# 🌳 Decision Tree Algorithms (Regression & Classification)

Decision Trees are supervised learning models used for both **regression and classification**.  
They work by **recursively splitting** the dataset into smaller subsets based on feature values.

---

## 5. Decision Tree (Regression)

### ✅ What is Decision Tree Regression?
Decision Tree Regression predicts a **continuous numerical value** (e.g., house price, temperature).  
It recursively splits the dataset into smaller regions to minimize prediction error.

---

### 🔁 Recursive Splits

- The tree starts from the **root node**.
- At each step (node), the algorithm chooses a feature and a value to split the data.
- It keeps splitting until:
  - max depth is reached, OR
  - minimum sample requirement is met.

> Goal: Find splits that minimize **variance** (error).

Example split:
If (Area < 2000 sq ft)
Predict lower price
Else
Predict higher price

---

### 📉 Entropy / Information Gain (Concept)

Although **regression trees typically use MSE (Mean Squared Error)**, entropy is an impurity measurement concept borrowed from classification.

- **Entropy** → measures disorder/impurity of data.
- **Information Gain** → reduction in impurity after a split.

Formula (for reference):
Information Gain = Entropy(parent) – Weighted Sum of Entropy(children)


> Higher information gain → better split.

---

### ✂️ Pruning (to avoid overfitting)

Decision trees grow until they perfectly fit the training data → **overfitting**.

Two types of pruning:

| Type | When? | Meaning |
|------|--------|---------|
| **Pre-Pruning** | during tree growth | Stop early (max_depth, min_samples_split) |
| **Post-Pruning** | after tree completes | Remove unnecessary branches |

Effect of pruning:

✅ reduces overfitting  
✅ improves generalization on test data

---

## 6. Decision Tree (Classification)

### ✅ What is Decision Tree Classification?
Used when output is **categorical** (0/1, Yes/No, Spam/Not Spam, etc.)

Example:
If Age > 45 and Cholesterol > 200
Predict: Heart Disease = Yes
Else
Predict: Heart Disease = No


---

### ✅ Splits (Gini / Entropy)

Decision Tree Classifier uses impurity metrics:

| Metric | Used in | Goal |
|--------|---------|------|
| **Entropy** | ID3 | Lower entropy = purer node |
| **Gini Index** | CART (most common) | Faster to compute |

Example:


The algorithm chooses the feature that results in **maximum purity**.

---

### ⚠️ Overfitting

Decision Trees tend to memorize training data (high depth).

Symptoms:

- Training accuracy = 100%
- Test accuracy = poor

Solution → **Regularization** using:

| Hyperparameter | Meaning |
|----------------|---------|
| max_depth | Limit the height of tree |
| min_samples_split | Minimum samples to split |
| min_samples_leaf | Minimum samples in a leaf |

> Smaller trees generalize better.

---

###  Confusion Matrix (performance evaluation)

Confusion matrix shows predictions vs. actual values:

|                | Predicted Positive | Predicted Negative |
|----------------|--------------------|--------------------|
| **Actual Positive** | True Positive (TP) | False Negative (FN) |
| **Actual Negative** | False Positive (FP) | True Negative (TN) |

From this matrix we get:

- **Accuracy**
- **Precision**
- **Recall**
- **F1 Score**

