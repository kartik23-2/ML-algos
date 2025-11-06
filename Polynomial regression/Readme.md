# 📘 Polynomial Regression with Regularization (Ridge & Lasso)

## ✅ Overview

Real-world datasets are often **non-linear**, meaning a straight line (Linear Regression) cannot properly capture the pattern.

➡️ **Polynomial Regression** helps model non-linear relationships  
➡️ **Regularization (Ridge / Lasso)** prevents overfitting

---

## ⭐ What is Polynomial Regression?

Polynomial Regression transforms the original input **X** into higher-degree polynomial terms:

Example:  
For input feature `x`, polynomial regression generates:

| Degree | Features Generated |
|--------|-------------------|
| 1      | 1, x              |
| 2      | 1, x, x²           |
| 3      | 1, x, x², x³       |

Thus, the model becomes:

\[
y = b_0 + b_1x + b_2x^2 + b_3x^3 + ... 
\]

📌 Even though equation becomes polynomial, we still use **Linear Regression internally**.

---

## ⚠️ Problem: Overfitting

When polynomial degree increases (example: degree = 5 or 10), the model:

- fits the training data perfectly
- learns noise instead of real patterns

❗ Result: **Training accuracy high, test accuracy low**

---

## ✅ Solution: Regularization

Regularization controls the **magnitude of model coefficients** so that the model does not become overly complex.

---

# 🔹 Ridge Regression (L2 Regularization)

> **“Reduce coefficient magnitude, but don’t eliminate features.”**

Ridge adds a penalty on squared coefficients:

\[
Loss = MSE + \alpha \sum w^2
\]

- `λ` (alpha) controls regularization strength
- Higher λ → more penalty → coefficients shrink

✅ Prevents overfitting  
❌ Does not remove features (no feature selection)

📌 Use when **all features contribute to output**.

---

# 🔹 Lasso Regression (L1 Regularization)

> **“Shrink some coefficients to zero — automatic feature selection.”**

Lasso penalizes the absolute value of weights:

\[
Loss = MSE + \lambda \sum |w|
\]

- Can make some coefficients **exactly zero**
- Works like built-in feature selection

✅ Prevents overfitting  
✅ Removes unimportant features  
✅ Useful when dataset has many features

📌 Use when you want **feature selection**.

---

##  Ridge vs Lasso (Summary)

| Feature / Behavior      | Ridge (L2)                     | Lasso (L1)                         |
|------------------------|----------------------------------|-------------------------------------|
| Shrinks coefficients   | ✅ Yes                          | ✅ Yes                              |
| Can set coefficients to zero | ❌ No                     | ✅ Yes (Feature selection)          |
| Best use case          | When many features matter        | When feature selection is needed    |

---

