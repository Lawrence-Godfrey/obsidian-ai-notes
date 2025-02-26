#flashcards

What is the purpose of the Attention mechanism in Seq2Seq models?
?
To enhance the capability of the models by allowing them to focus on different parts of the input sequence for each step of the output sequence.

What are the two primary types of attention mechanisms?
?
Global (or Soft) Attention and Local (or Hard) Attention.

What is the main advantage of Global Attention?
?
It considers all hidden states of the encoder when generating each word of the decoder, allowing for a thorough analysis of the input sequence.

What is a disadvantage of Global Attention?
?
It is computationally intensive.

How does Local Attention differ from Global Attention?
?
Local Attention focuses only on a subset of the encoder's hidden states, making it more efficient but potentially less accurate.

What roles do keys, values, and queries play in the Attention mechanism?
?
Keys and queries create a linear transformation of the input embedding for effective attention, while the values matrix is used to transform the similarity embeddings for predicting the next word.

What is scaled dot-product self-attention?
?
It involves computing the dot product of the keys and queries matrix to find similarity embeddings, adjusting these embeddings based on their context and finalizing with a dot product with the values matrix.

In multi-head attention, what is the main advantage of using multiple key, query, and value matrices?
?
It produces different embeddings from multiple sets, which are then concatenated, resulting in higher-dimensional embeddings.

What is one major challenge associated with the Attention mechanism?
?
Computational Complexity, particularly with global attention requiring processing of all encoder states for each decoder step.

How has the Attention mechanism evolved in the context of neural networks?
?
It has led to the development of the Transformer model, which utilizes attention mechanisms exclusively and has improved training efficiency and performance.

Why are memory requirements high when using Attention mechanisms for long sequences?
?
Attention mechanisms need to store and process all encoder states, leading to increased memory usage.

What recent model architecture relies entirely on attention mechanisms?
?
The Transformer model.

