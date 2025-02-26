#flashcards

What is the main contribution of the transformer architecture introduced by Vaswani et al. in 2017?
?
The transformer architecture revolutionized natural language processing, particularly sequence-to-sequence tasks like language translation, by using self-attention mechanisms that allow for parallel processing and greater efficiency compared to previous models.

What are the two main components of each encoder layer in a transformer model?
?
A multi-head self-attention mechanism and a position-wise fully connected feed-forward network.

Why is positional encoding important in transformers?
?
Positional encoding is crucial because transformers do not have an inherent sense of the order of tokens, so it provides the model with information about the relative or absolute position of tokens in the sequence.

What type of attention does the transformer model primarily use?
?
The transformer model uses scaled dot-product attention, and it also employs a multi-head attention mechanism.

How does the multi-head attention mechanism improve the performance of the transformer model?
?
Multi-head attention allows the model to simultaneously attend to different representation subspaces at various positions, offering a more nuanced understanding of context.

What role do layer normalization and skip connections play in the transformer architecture?
?
Layer normalization and skip connections help stabilize the training of deep networks by addressing issues of gradient flow and model convergence.

What is the purpose of the decoder in a transformer model?
?
The decoder generates the output sequence (e.g., a translated sentence) by attending to the encoder's output and applying its own attention mechanisms to produce coherent and contextually relevant results.

In what way has the transformer architecture changed the approach to processing large amounts of data?
?
Transformers allow for parallel processing of input data rather than sequential processing, significantly reducing training times and handling large datasets more effectively.

What does the embedding process in a transformer model involve?
?
The embedding process converts input tokens into vectors that capture semantic information, providing a meaningful numerical representation of each word.

What is the significance of removing recurrence in transformers compared to previous models?
?
Removing recurrence allows transformers to process data in parallel, leading to faster training times and more efficient computation compared to recurrent or convolutional models.

