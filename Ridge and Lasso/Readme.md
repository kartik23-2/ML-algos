##  Regularization --> Regularization is a technique used in machine learning to reduce overfitting by penalizing large coefficients (weights) in your model.(mtlb train data pe bohot accha krega pr test data pe acha ni krega).
1. 
## 🧩 Types of Regularization
1. L1 Regularization (Lasso)

Adds the absolute values of the coefficients as a penalty:

𝐿
𝑜
𝑠
𝑠
=
𝐸
𝑟
𝑟
𝑜
𝑟
+
𝜆
∑
∣
𝑤
𝑖
∣
Loss=Error+λ∑∣w
i
	​

∣

📉 Effect:

Forces some weights to become exactly 0

So it automatically performs feature selection (keeps only important features)

2️⃣ L2 Regularization (Ridge)

Adds the square of coefficients as a penalty:

𝐿
𝑜
𝑠
𝑠
=
𝐸
𝑟
𝑟
𝑜
𝑟
+
𝜆
∑
𝑤
𝑖
2
Loss=Error+λ∑w
i
2
	​


📉 Effect:

Shrinks large weights smoothly toward zero

Keeps all features but reduces their influence