Neural Networks are a class of machine learning models inspired by the human brain. They consist of interconnected nodes or "neurons" arranged in layers. A typical neural network comprises an input layer, one or more hidden layers, and an output layer. Each connection between the nodes has an associated weight, and each node applies a nonlinear activation function to its input before passing it on to the next layer.

### Forward Propagation
The output of a hidden layer $i$ can be computed by multiplying the matrix of weights with the vector output of the previous layer $i-1$:
$$Z_{i}= A_{i-1} W_{i} + b_{i}$$
The activation function is then applied to these outputs:
$$A_{i}= Activation(Z_{i})$$
### Backpropagation
The gradient of the output layer can be computed by calculating the difference between the activations of the final layer and the labeled outputs:
$$\delta_{L} = (\hat{Y} - Y)$$
where $L$ is the final layer.

The hidden layer losses can then be calculated by multiplying the weights $W_{i}$ by the gradients of the previously calculated layer $\delta_{i+1}$ and then element-wise multiplying the outcome with the derivative of the activation function:
$$\delta_{i}= (\delta_{i+1}W^{T}_{i}) \odot Activation'(Z_{i})$$
The weight deltas can be calculated from the gradients as follows:
$$\Delta W_{i}= -\alpha \times A^{T}_{i} \times \delta_{i+1}$$
