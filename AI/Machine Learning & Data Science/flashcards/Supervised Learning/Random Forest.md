#flashcards

Why do decision trees not generalize well?
?
Decision trees are very sensitive to samples in the data; a small change in the features of a sample can completely change the resulting tree.

What is Random Forest?
?
Random Forest is a supervised learning algorithm that builds an array (forest) of random decision trees using the bagging technique.

How does Random Forest create datasets for each tree?
?
For each tree, a new dataset is created by randomly sampling from the original dataset.

What is done regarding feature selection in Random Forest?
?
Each new dataset used for training a tree only includes a subset of the original features, which is usually the log or square root of the number of original features.

How does Random Forest make predictions?
?
When making predictions, a sample is passed through each tree, and the most common prediction across all trees is chosen.

Why does Random Forest reduce sensitivity to the dataset?
?
The random sampling and feature selection in Random Forest reduce the overall model's sensitivity to the specific samples in the dataset, helping it generalize better.

What technique is Random Forest an example of?
?
Random Forest is an example of bagging (Bootstrap Aggregating).

What is the purpose of using random sampling in Random Forest?
?
Random sampling helps create diverse datasets for each tree, reducing overfitting and improving generalization.

