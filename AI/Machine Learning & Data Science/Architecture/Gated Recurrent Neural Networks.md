Gated Recurrent Neural Networks (GRNNs) are an improved version of [[Recurrent Neural Networks|Recurrent Neural Networks]], specifically designed to deal with the issue of vanishing gradients and long-term dependencies in sequential data.

GRNNs utilise Gated Recurrent Units, which have an internal "Update Gate" and "Reset Gate" which the combined hidden state + input are fed into. These gates play a crucial role in determining how much information is retained from the previous hidden state and how much new information should be added from the current input.

![[Pasted image 20231220133221.png|center]]

Each of these gates have corresponding weights which are used to product outputs. The outputs of the gates are then recombined with the input and hidden state:
![[Pasted image 20231220133703.png]]

GRNNs are newer and slightly more efficient than [[Long-Short Term Memory networks]], since they only use a single internal cell state (the hidden state) and 2 gates, rather than 2 internal cell states and 3 gates. 

