Regularisation, also known as normalisation, is a technique used in machine learning to prevent overfitting and improve the generalisation of a model. Generally it involves adding a penalty term to the loss function during training.

## L1 Normalisation (L1 Regularisation)
 - L1 normalisation, also known as Lasso regularisation, involves adding a term to the loss function that penalises the model for the absolute value of the coefficients of the neural network weights.
 - The L1 regularisation term is the sum of the absolute values of the weights and is multiplied by a regularisation parameter (often denoted as λ or alpha). The modified loss function is given by:$$
	   L=L_0​+λ∑∣w∣
$$where $L_{0}$​ is the original loss function, $w$ represents the weights, and λ is the regularisation parameter.
 - L1 regularisation encourages sparsity in the weight matrix, meaning that it can lead to weights that are exactly zero. This can be useful for feature selection or creating simpler, more interpretable models.

## L2 Normalisation (L2 Regularisation)
 - L2 normalisation, also known as Ridge regularisation, adds a term to the loss function that penalises the model for the square of the magnitude of the coefficients.
 - The L2 regularisation term is the sum of the squares of the weights and is also multiplied by a regularisation parameter. The modified loss function with L2 regularisation is:
$$
L=L_0​+λ∑w2
	$$
	where the terms represent the same as in L1 regularisation.
 - Unlike L1 regularisation, L2 regularisation does not lead to sparse solutions; instead, it encourages the weights to be small but not necessarily zero. This can be useful for cases where we suspect many features contribute small amounts to the final prediction.

Both L1 and L2 regularisation help to prevent overfitting by penalising large weights, but they do so in different ways and have different effects on the model. They can also be used together, a technique known as Elastic Net regularization, which combines the properties of both L1 and L2 regularization. The choice between L1, L2, or a combination often depends on the specific characteristics of the problem and the dataset.