#flashcards

What is the output constraint for the hypothesis function in logistic regression?
?
$0 \leq h_{\theta}(x) \leq 1$.

What is the sigmoid function used in logistic regression?
?
$g(z) = \frac{1}{1+e^{-z}}$.

When do we predict that $y=1$ in logistic regression?
?
We predict $y=1$ if $h_{\theta}(x) \geq 0.5$.

What is the cost function used in logistic regression?
?
The cost function is the Log-Loss (Cross-Entropy Loss): $$J(h_{\theta},y)=-[y \log(h_{\theta}(x))+(1-y) \log(1-h_{\theta}(x))].$$

How is the cost function defined for $n$ samples in logistic regression?
?
$$J(\theta)=\frac{-1}{m}\sum_{i=1}^n[y^i \log(h_{\theta}(x^i))+(1-y^i) \log(1-h_{\theta}(x^i))].$$

What optimization technique is used to minimize the cost function in logistic regression?
?
Gradient Descent.

What regularization technique can be applied to logistic regression?
?
L2 (Ridge) regression is used for regularization.

What is the regularization term added to the logistic regression cost function?
?
$$\lambda \sum_{j=1}^{n} \theta_{j}^{2}.$$

What does 'One-vs-All' mean in multi-class classification?
?
Train $K$ separate binary classifiers, treating class $k$ as positive and all others as negative.

What are the advantages of the One-vs-All approach?
?
1. Simple to implement. 2. Each classifier can be trained independently (allows for parallelisation). 3. Works well for a moderate number of classes and balanced datasets.

What are the disadvantages of the One-vs-All approach?
?
1. May suffer from class imbalance. 2. Requires training $K$ classifiers, which can be computationally expensive. 3. Assumes that classes are mutually exclusive.

