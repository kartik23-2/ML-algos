
# Support Vector Machine
the main idea is to amximize the distance of training and and testing points from the hyperplane that is classifying in order to have wide range of classification for the new unseen data points.

1. we find the hyperplane on each side as parallel to main classifying hyperplane with the first '+ve' & '-ve' points on each side.
2. the distance between those 2 hyperplane is called margin(d) 
3. we find the hyperplane with that max value of margin(d).

#### support vectors are the points who decides the line(the nearest points)
##### w₁x₁ + w₂x₂ + b = 0 (think of a line)

##### Distance of apoint from line is ----->  |w·x + b| / ||w||

##### SVM wants to maximize the distance(margin) -----> Maximize margin = 2 / ||w||

###### But maximizing margin = minimizing ||w||.
###### So SVM tries to make weights small → simpler, more stable boundary.

###### This is the optimization.


### Hard Margin (perfectly separated classes)

If data is perfectly separable, SVM solves:

Minimize:   1/2 ||w||²
Subject to: yᵢ (w·xᵢ + b) ≥ 1


Meaning:

Points must be correctly classified

Margin must be at least 1 unit

 ### Soft Margin (real-life data with noise)

Real data always overlaps or has mistakes.

So SVM allows some violations using slack variables (ξ):

Minimize:  1/2 ||w||² + C Σ ξᵢ


###### Where:
### hyperparameter tuning
1. C = how strict SVM is

High C → fewer mistakes, small margin

Low C → more mistakes allowed, large margin

Big margin tends to generalize better.

2. Kernel (linear, poly, rbf, sigmoid)

Choose based on the nature of your data.

Data Pattern	Best Kernel
Linearly separable	Linear
Complex boundary, curved	RBF
Polynomial relation	Polynomial

3. Gamma (γ) — RBF / Polynomial Kernels

Controls how far the influence of a single training example reaches.

* High Gamma

Very small radius

Boundary too tight

Overfitting

* Low Gamma

Wider influence

Smoother boundary

Underfitting possible

### hyperplane

A hyperplane is a decision boundary that separates data points into classes.

In 2D, it’s a line

In 3D, it’s a plane

In higher dimensions, it’s a hyperplane

🔹 Goal of SVM: Find the Optimal Hyperplane

Among all possible separating boundaries, SVM chooses the one that creates the maximum margin between the classes.

## The Kernel Trick: The "Magic" for Non-Linear Data

This is the most brilliant part of SVM.

The Problem: If you can't draw a single line to separate the blue and red dots.

The "Trick": The SVM kernel trick uses a clever mathematical function to "project" your data into a higher dimension where it becomes linearly separable.

### The Analogy (The "Paper Pop"):

Imagine your 2D data is drawn on a flat piece of paper (a 2D plane). Red dots are in the center, and blue dots form a circle around them. You can't draw a line to separate them.
Now, what if you "pop" the paper up from underneath, pushing the red dots up into the 3rd dimension.
Suddenly, in this new 3D space, the red dots are "higher" than the blue dots.
Now, you can easily slice a flat plane (a 3D hyperplane) right through the middle, perfectly separating the two classes.
The kernel is the mathematical function that performs this "popping" (the projection). The "trick" is that the SVM algorithm can calculate the distances and relationships in that higher-dimensional space without ever actually creating and storing the data in that dimension. This saves an enormous amount of computation.

Common Kernels to Know:
1. 'linear': For data that is already linearly separable. This is the simple case we started with.
2. 'poly': The polynomial kernel. This is exactly like the PolynomialFeatures we used before. It creates features like X^2, X^3, etc., allowing it to find curved boundaries.
3. 'rbf' (Radial Basis Function): This is the default and most powerful kernel. It's a "Gaussian" kernel that can handle even very complex, "blob-like" shapes. It projects the data into an infinite-dimensional space, but it's very fast and efficient. ##Hyperparameter Tuning: Controlling Your SVM
When you use an rbf kernel, your goal is to find the best-fit boundary that isn't overfitting or underfitting. You control this using two main "knobs" (hyperparameters).