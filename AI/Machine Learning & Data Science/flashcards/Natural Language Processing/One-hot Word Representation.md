#flashcards

What is a one-hot vector?
?
A one-hot vector is a binary vector where all elements are zero except for one element, which is set to one, corresponding to a particular word.

What are the main advantages of using one-hot vectors?
?
1. Simplicity 2. No implied ordering of words.

What are the disadvantages of one-hot vectors?
?
1. Huge vectors that scale with vocabulary size. 2. No embedded meaning, making it impossible to compare words meaningfully.

Why can't one-hot vectors compare words meaningfully?
?
Because they do not provide any information about the relationships or similarities between words; each word is represented independently.

How do one-hot vectors scale with vocabulary size?
?
The size of the one-hot vector increases linearly with the size of the vocabulary; each additional word adds another dimension to the vector.

What does it mean that one-hot vectors have 'no implied ordering'?
?
It means that the representation does not reflect any relationships, hierarchy, or sequence between the words being represented.

Can you give an example of a one-hot vector for a three-word vocabulary: cat, dog, fish?
?
The one-hot vector for 'cat' would be [1, 0, 0], for 'dog' it would be [0, 1, 0], and for 'fish' it would be [0, 0, 1].

