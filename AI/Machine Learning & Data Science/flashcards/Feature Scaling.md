#flashcards

What is feature scaling?
?
Feature scaling is a technique used to normalize the range of values of features in a dataset, ensuring each feature contributes equally to the computation of the objective function.

What is the purpose of Min-Max Scaling?
?
Min-Max Scaling scales each feature to a given range, typically [0, 1] or [-1, 1], ensuring all features are on the same scale.

What is the formula for Min-Max Scaling?
?
X_scaled = (X - X_min) / (X_max - X_min), where X is the original feature vector, and X_min and X_max are the minimum and maximum values of each feature.

What does Mean Normalisation do?
?
Mean Normalisation transforms features to have a mean of zero.

What is the formula for Mean Normalisation?
?
X_scaled = (X - μ) / (X_max - X_min), where μ is the mean of the feature.

How can you perform feature scaling on an entire dataset at once?
?
You can perform feature scaling on an entire dataset by treating it as an m x n matrix and applying the scaling formulas to obtain scaled values for each feature.

What matrices are needed for scaling an m x n dataset?
?
For scaling an m x n dataset, you need the X_min and X_max matrices, which should have the same dimensions as the dataset, with the same min or max value repeated for each feature.

How do you obtain the min or max matrices for a dataset?
?
You obtain the min or max matrices by multiplying the transpose of X_min or X_max by a column vector of ones (1_m).

What are the benefits of feature scaling in machine learning?
?
Feature scaling helps algorithms that rely on distance calculations, such as k-nearest neighbors and gradient descent, to converge faster and perform better.

Can feature scaling affect the performance of a machine learning model?
?
Yes, unscaled features can disproportionately influence the performance of models sensitive to the magnitude of values, leading to suboptimal results.

