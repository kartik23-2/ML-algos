Ensemble learning combines multiple weak or strong models to create a more accurate and more stable final model.
Two major ensemble techniques are:

1. Bagging (Bootstrap Aggregating)

2. Boosting

Both improve model performance, but their approach is very different.
### How Bagging Works 

1. Take the original training dataset.

2. Create multiple bootstrap samples
(sampling with replacement → duplicates allowed).

3. Train a separate model on each bootstrap sample.

4. Combine predictions:

* **Classification** → majority vote

* **Regression** → average

#### Example: Random Forest

###### Random Forest = Decision Trees + Bagging + random feature selection.

###### This reduces overfitting and stabilizes predictions.


### how boosting works