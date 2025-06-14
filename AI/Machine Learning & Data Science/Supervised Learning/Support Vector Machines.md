Support Vector Machines (SVM) are supervised learning algorithms primarily used for classification, but they can also be adapted for regression tasks. The core idea behind SVM is to find the hyperplane that best separates two classes of data points in a high-dimensional space, with the "best" hyperplane being the one that maximises the margin between the nearest points of the two classes. These nearest points are known as support vectors.

### SVM vs. Logistic Regression

1. **Task**:
    - Both can be used for classification tasks. Logistic Regression can naturally output probabilities, whereas standard SVM does not output probabilities.
2. **Objective Function**:
    - Logistic Regression minimises the log-loss (or cross-entropy) function.
    - SVM minimises a function that aims to maximise the margin between support vectors of different classes.
3. **Probabilistic Interpretation**:
    - Logistic Regression has a probabilistic interpretation, as it models the conditional probability of the output class given the features.
    - SVM does not naturally provide probabilities, although techniques like Platt scaling can be applied to estimate probabilities.
4. **Regularisation and Loss**:
    - Both models use regularisation, but they use different loss functions—log-loss for Logistic Regression and hinge loss for SVM.
5. **Linear vs. Non-linear Boundaries**:
    - Logistic Regression models are generally linear classifiers but can model nonlinear boundaries using feature transformations or polynomial features.
    - SVM can easily handle non-linear boundaries by employing the "kernel trick," which implicitly maps the feature space to a higher-dimensional space.
6. **Computational Complexity**:
    - Logistic Regression is generally easier to train and scales well with large datasets.
    - Training an SVM, especially with a non-linear kernel, can be computationally expensive for large datasets.

![[Pasted image 20230828150431.png | center]]


![[Pasted image 20230828150635.png | center]]

### Kernels 
SVMs with kernels automatically adapt to non-linear relationships in the data by implicitly mapping the feature space to a higher-dimensional space where a separating hyperplane may exist (known as the "kernel trick").

![[Pasted image 20230828162307.png | center]]

Basically, instead of using a non-linear model, transform the data so that it can be separated by a non-linear.

#### SVM vs [[Logistic Regression]]
If your number of features $n$ is $\geq$ your number of training samples $m$, use logistic regression or SVM without a kernel (linear kernel).
If $n$ is small and $m$ is intermediate, use SVM with a gaussian kernel.
If $n$ is small and $m$ is large, create/add more features and then use logistic regression or an SVM.
