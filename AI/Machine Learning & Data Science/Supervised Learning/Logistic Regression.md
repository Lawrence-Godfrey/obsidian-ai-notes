## Binary Classification
Statistical method for predicting a categorical outcome $y$ where $y \in \{0, 1\}$.

Want $0 \leq h_{\theta}(x) \leq 1$ 
$$h_{\theta}(x) = g(\theta^{T} x )$$
where $$g(z) = \frac{1}{1+e^{-z}}$$
This logistic function is known as the Sigmoid function, and constrains the output of the objective function to a value between 0 and 1.

![[Pasted image 20230828123244.png | center]]

Predict $y=1$ if $h_{\theta}(x) \geq 0.5$

### Derivation
In a binary classification problem, we model the probability ppp that an outcome belongs to class 1 (e.g., success, positive class). The odds of this outcome occurring are defined as:
$$\text{Odds} = \frac{p}{1 - p}$$​To ensure that the output of the model can take any real number, we take the natural logarithm of the odds:
$$\text{Logit}(p) = \ln \left( \frac{p}{1 - p} \right)$$
The reason for taking the logarithm is that while probabilities $p$ range between 0 and 1, the log-odds transform maps this range to the entire real number line $(-\infty, \infty)$. This makes it suitable for a linear model.

Logistic regression assumes that the log-odds of the probability of success can be expressed as a linear function of the input features:
$$\ln \left( \frac{p}{1 - p} \right) = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \dots + \beta_n$$​This linearity makes the model interpretable and computationally convenient.
By exponentiating both sides, we can express the probability $p$ as:
$$p = \frac{e^{\beta_0 + \beta_1 x_1 + \dots + \beta_n x_n}}{1 + e^{\beta_0 + \beta_1 x_1 + \dots + \beta_n x_n}}$$
This is the **sigmoid function** (multiply the numerator and denominator by $e^{-z}$ if you don't see it), which ensures that the predicted probability remains in the range $(0,1)$. 
### Cost Function
The cost function used for Logistic Regression is the Log-Loss (or [[AI/Machine Learning & Data Science/Supervised Learning/Loss Functions#Cross-Entropy Loss|Cross-Entropy Loss]]), defined for a single sample as:

$$J(h_{\theta},y)=−[y \log(h_{\theta}(x))+(1−y) \log(1−h_{\theta}(x))]$$

For $n$ samples, the cost function is the average over all samples:

$$J(\theta)=\frac{-1}{m}\sum\limits_{i=1}^n​[y^i \log(h_{\theta}(x^i))+(1−y^i) \log(1−h_{\theta}(x^i))]$$

### Optimisation
[[Gradient Descent]] can be used to minimise the cost function with respect to the parameters.

### Regularised Logistic Regression
Similarly to regularised linear regression, logistic regression can be regularised using L2 (Ridge) regression by adding the following [[Regularisation]] term to the cost function:
$$\lambda \sum_{j=1}^{n} \theta_{j}^{2}$$
## Multi-class Classification
Predicting a single class, not to be confused with [[AI/Machine Learning & Data Science/Supervised Learning/Logistic Regression#Multi-label Classification|Multi-label Classification]], which can predict a number of classes.
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
#### Softmax Regression
A Multi-class classifier can also be created using Softmax regression, where the output logits are converted to a probability distribution with a [[AI/Machine Learning & Data Science/Supervised Learning/softmax|Softmax activation function]]. If you want a **single model** that naturally assigns a probability distribution over all classes, **Softmax regression is the better choice**. It directly optimises for **mutually exclusive** classes, ensuring that:
$$\sum_{j=1}^{n} \hat{y}_j = 1$$
This is useful when probabilities need to be comparable.

In this case [[AI/Machine Learning & Data Science/Supervised Learning/Loss Functions#Cross-Entropy Loss (aka Categorical Cross-Entropy)|Categorical Cross-Entropy Loss]] is used.
### Multi-label Classification
**Multi-label classification** refers to the task where each sample can belong to **multiple classes** simultaneously. Each label is treated as an independent binary classification problem.
- The sigmoid function is applied to each output neuron to convert the logits (raw model outputs) into probabilities.
- This gives a probability for each label, which is independent of other labels.
- [[AI/Machine Learning & Data Science/Supervised Learning/Loss Functions#Cross-Entropy Loss|Cross-Entropy Loss]] is used for 