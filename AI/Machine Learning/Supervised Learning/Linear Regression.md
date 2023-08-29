Linear regression is a statistical model that is used to understand the relationship between a dependent variable and one or more independent variables. A linear regression model outputs a continuous-valued prediction based on the input variables as opposed to a categorical or discrete prediction. 

## Cost Function
The cost function for linear regression is: $$J(\theta) = \frac{1}{2m} \sum_{i=1}^{m}  (h_{\theta}(x^{(i)}) - y^{(i)})^2$$
For a single variable $$h_{\theta}(x) = \theta_{0} + \theta_{1}x$$and for multiple variables you would have $$h_{\theta}(x)= \theta_{0} + \theta_{1}x_1 +  ... +\theta_{n}x_n $$
The vectorised form of the cost equation is $$J(\theta) = \frac{1}{2m}(X\theta - y)^T(X\theta - y)$$
where 
 - $y$ is the vector of labels.
 - $X$ is the $n\times m$ matrix of input features (sometimes called the design matrix) which includes the "intercept" feature, i.e., the constant features.
 - $\theta$ is the $m \times 1$ matrix of parameters.

Our goal is to minimise the cost function $J(\theta)$ with respect to $\theta$ (which just means we want to find the lowest value of $J$ by adjusting out parameters $\theta$). One method to do this is using gradient descent.

## Gradient Descent
[[Gradient descent]] is an algorithm used to minimise a function by iteratively moving in the direction of steepest descent. To find the "steepest descent" we need to first find the derivative of our cost function. 

Since our parameters can be multi-dimensional, we need to find the partial derivative with respect to each dimension
$$\frac{\delta}{\delta\theta_{j}} J (\theta) = \frac{1}{m}\sum\limits_{i=1}^m (h_\theta(x^{i})- y^i)\cdot x^i$$
and update them all at once before moving on to the next iteration. 
$$\theta_{j} := \theta_{j} - \alpha \frac{\delta}{\delta\theta_{j}} J (\theta)$$
where 
 - $\alpha$ is the learning rate, which is a hyper-parameter which controls how much the parameters should be adjusted each iteration. Too low a value causes gradient descent to happen slowly, while too large a value will prevent gradient descent from converging and could cause it to diverge.

The vectorised form of this equation is $$\nabla J(\theta) = \frac{1}{m}X^{T}(X\theta - y)$$
and the update equation would be
$$\theta := \theta - \alpha \nabla J(\theta)$$
### Batch Gradient Descent
This algorithm is known as "Batch" gradient descent, meaning each step of gradient descent makes use of the entire training set. This is obviously quite computationally expensive, and more efficient variations like Stochastic gradient descent and mini-batch gradient descent have been developed to solve this issue.

### The Normal Equation
The Normal equation is a method to minimise your cost function analytically. 
$$\theta = (X^{T}X ) ^{-1} X^{T} y$$
While this may seem like a nice solution since you don't need to choose a learning rate or iterate, it can be very slow as the dataset increases due to the computationally expensive operation $$(X^{T}X)^{-1}$$
### Regularised Linear Regression
L2 (Ridge) regularisation can be applied to the linear regression cost function as follows:
$$ J(\theta) = \frac{1}{2m}[\sum_{i=1}^{m}  (h_{\theta}(x^{(i)}) - y^{(i)})^{2}+ \lambda \sum_{j=1}^{n} \theta_{j}^{2}]$$
The partial derivative of the cost function with regularisation would then be $$\frac{\delta}{\delta\theta_{j}} J (\theta) = \frac{1}{m}\sum\limits_{i=1}^m (h_\theta(x^{i})- y^i)\cdot x^{i}+ \frac{\lambda}{m}\theta_j$$
Or, in its vectorised form:
$$\nabla J(\theta) = \frac{1}{m}X^{T}(X\theta - y) + \lambda \theta$$
