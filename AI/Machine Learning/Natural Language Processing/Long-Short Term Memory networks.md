Long-Short Term Memory (LSTM) units are a type of [[Recurrent Neural Networks|Recurrent Neural Network]] (RNN) architecture that is specifically designed to handle the vanishing gradient problem. This architecture was invented in 1997, and consist of a series of gates to regulate the flow of information within the network. 

LSTM units consist of three main gates: the input gate, the forget gate, and the output gate. 
 - The forget gate essentially decides what percentage (using sigmoid activation) of the long-term memory (cell state) is remembered, based on the short-term memory and the input. This can be useful in longer sequences where certain information at the start of the sequence is no longer relevant. 
 - The input gate uses a $sigmoid$ and $tanh$ activation function to determine how to update the long-term memory/cell state.
 - The output gate determines what short-term memory will be fed into the next unit, based on the current short-term memory, the input, and the updated long-term memory.

Essentially, the unit discards any irrelevant memory, adds new important information, and produces an output to the next unit.

![[Pasted image 20231222084851.png]]

LSTM units have a cell state, also known as the memory cell, which is responsible for storing and maintaining long-term information. This cell state does not flow through any weights between units, and therefore does not have the vanishing/exploding gradient problem. There is also a short-term memory, which is fed directly into the gates, rather than propagating through all the units. 