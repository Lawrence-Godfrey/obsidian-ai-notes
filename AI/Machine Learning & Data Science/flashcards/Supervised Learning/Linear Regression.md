#flashcards

What is the purpose of linear regression?
?
To understand the relationship between a dependent variable and one or more independent variables.

What type of prediction does linear regression output?
?
Continuous-valued prediction.

What is the cost function for linear regression?
?
J(θ) = (1/2m) Σ (h_θ(x^(i)) - y^(i))^2.

Write the hypothesis function for a single variable linear regression.
?
h_θ(x) = θ₀ + θ₁x.

What is the vectorized form of the cost function in linear regression?
?
J(θ) = (1/2m)(Xθ - y)ᵀ(Xθ - y).

Define the components of the matrix X in linear regression.
?
X is the n x m matrix of input features including the intercept feature.

What is the goal when using the cost function J(θ) in linear regression?
?
To minimize the cost function J(θ) with respect to θ.

What is gradient descent used for in the context of linear regression?
?
To minimize the cost function by iteratively moving in the direction of steepest descent.

What does the learning rate α control in gradient descent?
?
It controls how much the parameters should be adjusted in each iteration.

What is batch gradient descent?
?
An algorithm that uses the entire training set for each step of gradient descent.

What is the normal equation in linear regression?
?
θ = (XᵀX)⁻¹ Xᵀy.

What is the effect of applying L2 regularization (Ridge) to the cost function?
?
It penalizes large coefficients to improve the model's generalization.

How does the partial derivative of the cost function change with regularization?
?
It adds a term λ/m θₓ to the original partial derivative.

What is the vectorized form of the gradient with regularization in linear regression?
?
∇J(θ) = (1/m)Xᵀ(Xθ - y) + λθ.

What are the potential downsides of the Normal Equation method for linear regression?
?
It can be very slow as the dataset increases due to the computationally expensive operation (XᵀX)⁻¹.

What are two efficient variations of gradient descent mentioned?
?
Stochastic gradient descent and mini-batch gradient descent.

