##  Regularization --> Regularization is a technique used in machine learning to reduce overfitting by penalizing large coefficients (weights) in your model.

(mtlb train data pe bohot accha krega pr test data pe acha ni krega).

##  Types of Regularization

1. L1 Regularization (Lasso)

Adds the absolute values of the coefficients as a penalty:

### Effect:

Forces some weights to become exactly 0

So it automatically performs feature selection (keeps only important features)

2. L2 Regularization (Ridge)

Adds the square of coefficients as a penalty:

### Effect:

Shrinks large weights smoothly toward zero

Keeps all features but reduces their influence