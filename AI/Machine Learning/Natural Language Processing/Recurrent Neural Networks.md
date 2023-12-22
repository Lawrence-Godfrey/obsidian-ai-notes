Recurrent Neural Networks (RRNs) are a type of artificial neural network that is designed to process sequential data. RNNs do not have a fixed-length input size, and can process a variable-sized input, making them suitable for tasks such as speech recognition, natural language processing, and time series analysis.

RNNs can be used to classify a sequence (many-to-one), translate a sequence (many-to-many), and even generate a sequence from a single input (one-to-many).
![[Pasted image 20231220114658.png]]

RNNs consist of a core recurrent cell or block which takes in an input which is combined with its internal hidden state to product an output. At each time-step the internal state is updated based on the input and some internal weights (FCNN). 

Another way to think about this is to "unroll" the network and show the hidden states as outputs of recurrent blocks which get fed into the next recurrent block:
![[Pasted image 20231220115907.png]]

There are usually weights between the input and the recurrent block, as well as between the hidden state and the next block, and between the block and the output. 

For machine translation, a one-to-many encoder-decoder style architecture can be used, where the encoder processes the input sequence and produces a final output vector, which the decoder uses to produce an output sequence:
![[Pasted image 20231220120447.png|center]]

## Loss and Testing
Loss is generally calculated on every output at each time-step, and combined together to get a final loss value. 
During testing, the correct/target output is usually fed into the next recurrent block even if the previous output was incorrect. This is to avoid the error compounding on itself over the time-steps (each step using the previous, incorrect output to produce the next).

## Gradient Descent
It can be incredibly inefficient to do gradient descent on an entire sequence, since you need to go through the entire sequence, computer the loss using all the outputs, and then do a single step of gradient descent backwards. If you're processing a large sequence (lets say the whole of Wikipedia, then this can be incredibly slow). 
Instead, an approximation, Truncated Backpropagation through time is used, where only a chunk of the sequence is used at a time, similar to Mini-batch Gradient Descent.
## Drawbacks
The major drawbacks to using RNNs are their susceptibility to vanishing and exploding gradients, limited ability to capture long-term dependencies, and high computational requirements (can't use much parallel computing since it needs to be done sequentially).
### Exploding Gradient
You can imaging that for longer sequences, a large scaler value in the weight matrix (which is shared) will cause a value >1 to explode in size as the gradient moves backwards through the many recurrent units and gets repeatedly multiplied by the same large scaler.

There are some hacks to combat the exploding gradient problem, like gradient clipping, but for the vanishing gradient problem, more complex architectures are required, like [[Gated Recurrent Neural Networks]] and [[Long-Short Term Memory networks]]

