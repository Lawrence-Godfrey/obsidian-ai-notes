#flashcards

What is the main advantage of Gated Recurrent Neural Networks (GRNNs) over traditional Recurrent Neural Networks (RNNs)?
?
GRNNs are designed to deal with the issue of vanishing gradients and long-term dependencies in sequential data.

What are the two main components of Gated Recurrent Units (GRUs) in GRNNs?
?
The two main components are the Update Gate and the Reset Gate.

How do the gates in GRNNs affect information flow?
?
The gates determine how much information is retained from the previous hidden state and how much new information is added from the current input.

Compare the internal state management between GRNNs and Long-Short Term Memory networks (LSTMs).
?
GRNNs use a single internal cell state (the hidden state) and 2 gates, while LSTMs use 2 internal cell states and 3 gates.

What role do the weights play in Gated Recurrent Units?
?
The weights are used to produce outputs from the gates.

Why are GRNNs considered slightly more efficient than LSTMs?
?
Because GRNNs only require one internal cell state and two gates instead of two internal cell states and three gates.

What problem in machine learning do GRNNs specifically address?
?
GRNNs specifically address the problem of vanishing gradients in sequential data processing.

Describe the process through which inputs and hidden states are combined in GRNNs.
?
The outputs of the Update and Reset gates are combined with the current input and hidden state to update the network's state.

