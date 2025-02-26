#flashcards

What are Recurrent Neural Networks (RNNs) primarily used for?
?
RNNs are used to process sequential data such as speech recognition, natural language processing, and time series analysis.

How do RNNs handle input sizes?
?
RNNs do not have a fixed-length input size, allowing them to process variable-sized input.

What are the three types of outputs RNNs can produce with sequences?
?
RNNs can classify a sequence (many-to-one), translate a sequence (many-to-many), and generate a sequence from a single input (one-to-many).

What is the architecture of an RNN?
?
An RNN consists of a core recurrent cell or block that takes in an input, combines it with its internal hidden state, and produces an output.

Explain the concept of 'teacher forcing' in RNN training.
?
Teacher forcing involves feeding the correct target output into the next recurrent block during training, which helps prevent error compounding across time-steps.

What is a significant challenge with gradient descent in RNNs?
?
Performing gradient descent on an entire sequence can be inefficient due to the large size and complexity of the sequences.

What is Truncated Backpropagation Through Time?
?
It's an approximation method for training RNNs where only a chunk of the sequence is used at a time to make the training process more efficient.

What are the major drawbacks of RNNs?
?
RNNs are susceptible to vanishing and exploding gradients, have limited ability to capture long-term dependencies, and have high computational requirements.

What is the exploding gradient problem in RNNs?
?
The exploding gradient problem occurs when large scaler values in the weight matrix cause the gradients to exponentially increase during backpropagation.

Name two architectures that help mitigate the vanishing gradient problem in RNNs.
?
Gated Recurrent Neural Networks (GRNNs) and Long Short-Term Memory networks (LSTMs) are two architectures designed to address the vanishing gradient problem.

