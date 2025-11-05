### Linear Regression is a supervised learning algorithm used to predict a continuous outcome variable (Y) based on one or more input features (X).

It assumes a linear relationship between the dependent and independent variables.

##  Simple Linear Regression (SLR)
 Definition-->

Uses one independent variable to predict the target variable.

 Example-->

Predicting salary from years of experience.

 Visualization

A straight line best fitting the data points in a 2D graph.

## Multiple Linear Regression (MLR)
 Definition-->

Uses two or more independent variables to predict the target variable.

 Example-->

Predicting house price using area, number of bedrooms, and age.

 Visualization-->

Represents a plane (or hyperplane) in higher dimensions (not easily visualizable beyond 3D).

# Model evaluation

1. r2_score --> Measures how well features explain target variance.

Ranges from 0 to 1.

1 → perfect prediction

0 → no linear relationship

2. MSE --> Measures average squared difference between actual and predicted values.

Lower MSE = better model.

# Coefficient and Intercept

intercept--> it is base prediction when all input is zero.

Coefficient --> Change in prediction for a 1-unit change in the respective feature mtlb konsa feature kitna effect krega(slope)

# Insight

1. need better treatment for outliers or simply overfitting
