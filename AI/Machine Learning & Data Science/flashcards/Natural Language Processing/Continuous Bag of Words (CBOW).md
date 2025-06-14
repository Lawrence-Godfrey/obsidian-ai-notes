#flashcards

What is the main purpose of the Continuous Bag of Words (CBOW) model?
?
The CBOW model learns to predict a target word based on its surrounding context words.

How does CBOW differ from supervised learning models?
?
CBOW is a self-supervised model that does not require labeled data for training but learns from the structure of the text itself.

What is used as the input and output in the CBOW model during training?
?
Context words are used as input, and the center word is used as the label (output).

What type of word representation does the CBOW model use to vectorize words?
?
The CBOW model uses One-hot word representation to vectorize the center and context words.

What is the size of the input and output layers in the CBOW model?
?
Both the input and output layers are of size V, where V is the size of the vocabulary.

What activation functions are used in the CBOW model?
?
The first activation function is ReLU, and the second is softmax.

What type of loss function is used to train the CBOW model?
?
Cross-entropy loss is used to train the CBOW model.

How can word embeddings be extracted from a trained CBOW model?
?
Word embeddings can be extracted from the weight matrix W1 between the input layer and hidden layer, or from the rows of the weight matrix W2 between the hidden layer and output layer. You can also average W1 and the transpose of W2.

What are intrinsic and extrinsic evaluation methods used for in the context of CBOW word embeddings?
?
These methods are used to evaluate the quality of the word embeddings generated from the CBOW model.

Describe the architecture of a CBOW model. What is its main component?
?
The architecture consists of an input layer, a hidden layer, and an output layer, with the main component being a shallow dense neural network.

