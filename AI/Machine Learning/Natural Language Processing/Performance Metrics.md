## Perplexity
Perplexity is the measure of how well a probability distribution or a language model predicts a sample of text.
$$
		PP(W) = P(s_{1}, s_{2}, ..., s_{m})^{-\frac{1}{m}}
$$
Where:
 - $W$ is a test set containing $m$ sentences $s$
 - $s_i$ is the $ith$ sentence in the test set, ending with `</s>`
 - $m$ is the number of all words in the entire test set $W$

A very accurate model might have a perplexity score close to 1 on a test set, while a bad model might have a score in the hundreds. Good models can have perplexity scores between 20 and 50.

 - Sometimes log perplexity $logPP$ is used instead.
 - Only use the perplexity metric when comparing two models which have the same vocabulary. 
## Word Embeddings
### Intrinsic Evaluation
In the context of word embeddings, intrinsic evaluation refers to the assessment of word embeddings based on their internal properties and characteristics. This evaluation method focuses on analysing the quality and usefulness of word embeddings without considering their specific applications or external tasks. For example, intrinsic evaluation may involve measuring the semantic similarity between words, or identifying analogies or word relationships.
### Extrinsic Evaluation
Extrinsic evaluation, on the other hand, involves assessing word embeddings based on their performance in specific external tasks or applications. 