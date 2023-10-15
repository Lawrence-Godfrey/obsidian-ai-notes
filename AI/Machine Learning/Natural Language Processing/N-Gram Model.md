An N-gram is a sequence of N consecutive words or characters within a given text. For example, in the sentence "I love to eat ice cream," the 2-grams/bi-grams would be "I love," "love to," "to eat," "eat ice," and "ice cream.  

### N-gram Probability
We can build a simple N-gram model which produces a probability for a word given an N-gram. 
The probability of the last word appearing in an N-gram is given by:
$$P(w_{N}|w_{1}^{N-1}) = \frac{C(w_{1}^{N-1}w_{N})}{C(w_{1}^{N-1})}$$
I.e., the probability of the word occurring is the number of times the sequence appears in the corpus divided by the number of times the first $N-1$ words appear in the corpus.

### Probability of a Sequence
When calculating the probability of a sequence of words occurring together can be calculated using the [[Chain Rule]], since each word is interdependent on one another. Intuitively, the probability of a sequence is the conditional probability of each word, given the previous words in the sequence.

#### Approximation of Sequence Probability
However, this is limited by the fact that your corpus will likely not contain each sequence of words required to calculate all the products in the chain rule. As soon as one of the products is 0, the entire probability becomes 0.

We can approximate the probability by shortening the sequences in the conditional probabilities to a fixed length. For example, instead of looking at all the previous words in the sequence, we can just look at the previous word (i.e., the bi-gram). This approach, known as the Markov assumption, allows us to simplify the calculations and make them more computationally efficient.

So, instead of each probability being calculated as $P(w_{n}|w_{1}^{n-1})$ we can approximate it as $P(w_{n}|w_{n-N-1}^{n-1})$.