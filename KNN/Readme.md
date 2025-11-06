
---

## 📏 Distance Metrics (very important)

KNN depends on distance calculation to find nearest neighbors:

| Distance Metric | Description | Formula |
|----------------|-------------|---------|
| **Euclidean** (default) | Straight-line distance | `sqrt((x2-x1)^2 + (y2-y1)^2)`
| **Manhattan** | Block/step distance | `|x2-x1| + |y2-y1|`
| **Minkowski** | General form of Euclidean & Manhattan | Generalized power `p`

> Choice of distance metric impacts model accuracy.

---

## 🔧 Tuning K-value (hyperparameter tuning)

The value of **K** controls the complexity of the model:

| K Value | Effect |
|---------|--------|
| Small K (e.g., k = 1) | Highly sensitive → **overfitting**
| Large K (e.g., k = 20) | Too generalized → **underfitting**

✅ Finding optimal K is important → use **GridSearchCV** or plot Accuracy vs K.

---

