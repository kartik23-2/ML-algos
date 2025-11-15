
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

C = how strict SVM is

High C → fewer mistakes, small margin

Low C → more mistakes allowed, large margin

Big margin tends to generalize better.