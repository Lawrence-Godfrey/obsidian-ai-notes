#flashcards

What is ensemble learning?
?
Ensemble learning is a technique that combines multiple models to improve performance, often combining weak models to create a stronger overall model.

What is Bagging in the context of ensemble learning?
?
Bagging, or Bootstrap Aggregating, is an ensemble method where multiple versions of a model are trained independently on different subsets of the dataset created through bootstrapping.

How does Bagging improve model performance?
?
Bagging improves performance by averaging predictions for regression tasks or using majority vote for classification, which helps to reduce variance and mitigate overfitting.

Why does Bagging work well for decision trees?
?
Bagging works well for decision trees because decision trees tend to overfit when used alone, so combining multiple trees through Bagging creates a more robust model.

What is the main difference between Bagging and Boosting?
?
The main difference is that Bagging trains multiple models independently on different subsets of data, while Boosting trains models sequentially, with each model focusing on correcting the errors of the previous one.

What is Boosting in the context of ensemble learning?
?
Boosting is an ensemble technique where models are trained in sequence, with each model attempting to correct the errors made by its predecessors.

How does Boosting address bias in model training?
?
Boosting addresses bias by adjusting the focus on the misclassified data points from previous iterations, allowing subsequent models to learn from those mistakes.

What are some popular Boosting algorithms?
?
Popular Boosting algorithms include AdaBoost, Gradient Boosting, and XGBoost.

What is bootstrapping in the context of Bagging?
?
Bootstrapping is a sampling method where subsets of data are created by sampling with replacement, allowing the same data points to appear multiple times in different datasets.

How are predictions combined in Bagging for regression tasks?
?
For regression tasks in Bagging, the predictions from multiple models are averaged together.

How are predictions combined in Bagging for classification tasks?
?
For classification tasks in Bagging, the predictions from multiple models are combined using majority vote.

