#flashcards

What is regularisation in the context of machine learning?
?
Regularisation is a technique used in machine learning to prevent overfitting and improve the generalisation of a model by adding a penalty term to the loss function during training.

What does L1 regularisation (Lasso) penalise in a model?
?
L1 regularisation penalises the absolute value of the coefficients of the weights in a model.

What is the formula for the modified loss function in L1 regularisation?
?
The modified loss function is given by: L = L0 + λ∑|w|, where L0 is the original loss function, w represents the weights, and λ is the regularisation parameter.

What effect does L1 regularisation have on the weight matrix?
?
L1 regularisation encourages sparsity in the weight matrix, leading to some weights being exactly zero, which can be useful for feature selection.

What does L2 regularisation (Ridge) penalise in a model?
?
L2 regularisation penalises the square of the magnitude of the coefficients of the weights in a model.

What is the formula for the modified loss function in L2 regularisation?
?
The modified loss function is: L = L0 + λ∑w^2, where L0 is the original loss function, w represents the weights, and λ is the regularisation parameter.

How does L2 regularisation influence weight coefficients compared to L1 regularisation?
?
Unlike L1 regularisation, L2 regularisation does not lead to sparse solutions; it encourages weights to be small but not necessarily zero.

What is Elastic Net regularization?
?
Elastic Net regularization is a technique that combines the properties of both L1 and L2 regularisation.

In what scenarios might you prefer L1 regularisation over L2 regularisation?
?
You might prefer L1 regularisation in scenarios where feature selection is important and when you expect many weights to be exactly zero.

Why is regularisation important in machine learning models?
?
Regularisation is important because it helps to prevent overfitting by penalising large weights, which can lead to better generalisation of the model.

What are the common notations for the regularisation parameter in L1 and L2 regularisation?
?
The regularisation parameter is often denoted as λ (lambda) or alpha.

