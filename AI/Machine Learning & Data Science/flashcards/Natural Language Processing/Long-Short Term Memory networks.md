#flashcards

What is the primary purpose of Long-Short Term Memory (LSTM) units?
?
To handle the vanishing gradient problem in Recurrent Neural Networks (RNNs).

What year were LSTM units invented?
?
1997.

What are the three main gates in an LSTM unit?
?
The input gate, the forget gate, and the output gate.

How does the forget gate contribute to the LSTM's functionality?
?
It decides what percentage of long-term memory (cell state) to retain based on short-term memory and input.

What activation functions do the input gate of an LSTM use?
?
Sigmoid and tanh activation functions.

What does the output gate of an LSTM do?
?
It determines what short-term memory will be sent to the next unit based on current short-term memory, input, and updated long-term memory.

What is the role of the cell state in LSTM units?
?
It stores and maintains long-term information without being affected by weights between units.

How does the LSTM avoid the vanishing/exploding gradient problem?
?
The cell state does not flow through weights between units, thus maintaining its information over time.

What type of information does the short-term memory in LSTMs work with?
?
It is fed directly into the gates rather than propagating through all the units.

Why is it important for LSTM units to discard irrelevant memory?
?
To ensure that the network focuses on updating and maintaining only important information for better performance on longer sequences.

