#flashcards

What is the primary purpose of Support Vector Machines (SVM)?
?
SVM are supervised learning algorithms primarily used for classification tasks.

How do Support Vector Machines (SVM) determine the best hyperplane for classification?
?
SVM find the hyperplane that best separates two classes by maximizing the margin between the nearest data points, known as support vectors.

What is the key difference between SVM and Logistic Regression in terms of output?
?
Logistic Regression outputs probabilities, while standard SVM does not naturally provide probabilities.

What is the objective function used in Logistic Regression?
?
Logistic Regression minimizes the log-loss (or cross-entropy) function.

What type of loss function does SVM use?
?
SVM uses hinge loss.

What is the benefit of the 'kernel trick' in SVMs?
?
The kernel trick allows SVMs to handle non-linear relationships in the data by implicitly mapping the feature space to a higher-dimensional space.

When should you use logistic regression according to the number of features (n) and training samples (m)?
?
If the number of features n is greater than or equal to the number of training samples m, use logistic regression.

In what scenario should SVM with a Gaussian kernel be applied?
?
SVM with a Gaussian kernel should be used if the number of features n is small and the number of training samples m is intermediate.

How do SVM and Logistic Regression differ in handling large datasets?
?
Logistic Regression is easier to train and scales well with large datasets, while training an SVM can be computationally expensive, especially with non-linear kernels.

What form of regularization do both SVM and Logistic Regression use?
?
Both models use regularization but utilize different loss functions.

What must be done to handle non-linear boundaries in Logistic Regression?
?
Non-linear boundaries in Logistic Regression can be modeled using feature transformations or polynomial features.

What are support vectors in the context of SVM?
?
Support vectors are the nearest points to the hyperplane that help define the margin in SVM classification.

Describe how SVMs adapt to data with non-linear relationships.
?
SVMs adapt to non-linear relationships by using kernels to transform the data into a higher-dimensional space where a separating hyperplane may exist.

