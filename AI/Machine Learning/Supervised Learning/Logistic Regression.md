Statistical method for predicting a categorical outcome $y$ where $y \in \{0, 1\}$.

Want $0 \leq h_{\theta}(x) \leq 1$ 
$$h_{\theta}(x) = g(\theta^{T} x )$$
where $$g(z) = \frac{1}{1+e^{-z}}$$
This logistic function is known as the Sigmoid function, and constrains the output of the objective function to a value between 0 and 1.

![[Pasted image 20230828123244.png | center]]

Predict $y=1$ if $h_{\theta}(x) \geq 0.5$

### Cost Function
The cost function used for Logistic Regression is the Log-Loss (or Cross-Entropy Loss), defined for a single sample as:

$$J(h_{\theta},y)=−[y \log(h_{\theta}(x))+(1−y) \log(1−h_{\theta}(x))]$$

For $n$ samples, the cost function is the average over all samples:

$$J(\theta)=\frac{-1}{m}\sum\limits_{i=1}^n​[y^i \log(h_{\theta}(x^i))+(1−y^i) \log(1−h_{\theta}(x^i))]$$

### Optimisation
[[Gradient descent]] can be used to minimise the cost function with respect to the parameters.

### Regularised Logistic Regression
Similarly to regularised linear regression, logistic regression can be regularised using L2 (Ridge) regression by adding the following regularisation term to the cost function:
$$\lambda \sum_{j=1}^{n} \theta_{j}^{2}$$

### Multi-class Classification

#### One-vs-All
The "One-vs-All" (OvA), also known as "One-vs-Rest" (OvR), is a strategy for using binary classification algorithms for multi-class classification problems.

Suppose you have a classification problem with $k$ classes labeled $1,2,...,K$. In the One-vs-All method, you train $K$ separate binary classifiers. For each classifier $k$, you treat class $k$ as the "positive" class (label it as 1) and combine all the other classes as the "negative" class (label them as 0).

To classify a new input $x$, you would run it through all $K$ classifiers and predict the class of the classifier that outputs the highest probability.

##### Advantages and Disadvantages
- **Advantages**:
    1. Simple to implement.
    2. Each classifier can be trained independently, which allows for parallelisation.
    3. Works well when the number of classes $K$ is not too large and the classes are roughly balanced.
- **Disadvantages**:
    1. May suffer from class imbalance because each binary classifier is trained on an imbalanced dataset.
    2. Requires training $K$ classifiers, which may be computationally expensive if $K$ is large or the dataset is large.
    3. Assumes that classes are mutually exclusive, which may not be the case in all scenarios.