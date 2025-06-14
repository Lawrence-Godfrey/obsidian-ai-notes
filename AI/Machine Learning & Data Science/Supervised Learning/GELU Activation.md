The activation function referred to as the Gaussian Error Linear Unit (GELU) is defined by:

$$\text{GELU}(x) = x \cdot \Phi(x)$$

where $\Phi(x)$ is the cumulative distribution function of the standard normal distribution. A commonly used approximation is:

$$\text{GELU}(x) \approx 0.5x \left(1 + \tanh\left(\sqrt{\frac{2}{\pi}}(x + 0.044715x^3)\right)\right)$$

GELU is a smooth, non-linear activation that blends properties of ReLU and sigmoid, allowing small negative values to pass through rather than zeroing them out as ReLU does. It’s particularly popular in transformer architectures like BERT and GPT.

GELU is differentiable everywhere and has a smooth curve, meaning no abrupt changes like ReLU’s hard zeroing for x<0x < 0x<0. This improves optimisation stability, especially in deep or complex architectures.

Small negative activations can still carry useful signal. ReLU discards this entirely, potentially losing subtle features. GELU retains and attenuates them—so the network can _learn_ whether to keep or suppress them, instead of making a hard-coded choice.

![[Pasted image 20250407175645.png]]