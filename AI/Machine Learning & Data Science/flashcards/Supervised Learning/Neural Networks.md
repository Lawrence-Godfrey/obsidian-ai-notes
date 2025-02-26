#flashcards

What are the main components of a typical neural network?
?
A typical neural network consists of an input layer, one or more hidden layers, and an output layer.

What is the purpose of weights in a neural network?
?
Weights determine the strength of the connections between nodes and influence the output of the neural network.

How is the output of a hidden layer calculated?
?
The output of a hidden layer is calculated by multiplying the matrix of weights with the vector output of the previous layer and adding the bias term: Z_{i}= A_{i-1} W_{i} + b_{i}.

What role does an activation function play in neural networks?
?
An activation function introduces non-linearity to the model by transforming the output of the nodes before passing it to the next layer.

Describe the forward propagation process in neural networks.
?
In forward propagation, each node computes its output by applying an activation function to the weighted sum of inputs from the previous layer.

What is backpropagation used for?
?
Backpropagation is used to calculate the gradients of the loss function with respect to the weights in order to update the weights during training.

What formula is used to calculate the gradient of the output layer?
?
The gradient of the output layer is calculated as: δ_{L} = (Ŷ - Y), where L is the final layer, Ŷ is the predicted output, and Y is the actual labeled output.

How do you calculate the hidden layer loss in backpropagation?
?
The hidden layer losses are calculated using the formula: δ_{i}= (δ_{i+1}W^{T}_{i}) ⊙ Activation'(Z_{i}).

What is the purpose of the weight delta (ΔW) calculation?
?
The weight delta (ΔW) is calculated to update the weights in the direction that reduces the loss function, using the formula: ΔW_{i}= -α × A^{T}_{i} × δ_{i+1}, where α is the learning rate.

Who won the Nobel Prize in Physics in 2024 for work related to artificial neural networks?
?
Geoffrey Hinton won the Nobel Prize in Physics in 2024 for his work related to artificial neural networks.

