An N-gram is a sequence of N consecutive words or characters within a given text. For example, in the sentence "I love to eat ice cream," the 2-grams/bi-grams would be "I love," "love to," "to eat," "eat ice," and "ice cream.
## N-gram Probability
We can build a simple N-gram model which produces a probability for a word given an N-gram. 
The probability of the last word appearing in an N-gram is given by:
$$P(w_{n}|w_{n-N+1}^{n-1}) = \frac{C(w_{n-N+1}^{n-1}, w_{n})}{C(w_{n-N+1}^{n-1})}$$
I.e., the probability of the word occurring is the number of times the N-gram appears in the corpus divided by the number of times the $N-1$ gram appear in the corpus.

We can build this model by going through the corpus with a sliding window of size $N$ and building a set of unique $N-1$ grams and the number of times each word follows the $N-1$ gram.
For example, if our corpus is `<s> Humans and machines are not so different </s>` and we're building a tri-gram model, we would build up a set of unique bi-grams `<s> Humans`, `Humans and`, etc. and the number of times each word shows up after those. 

We can then sum each row, and divide all the cells by the row sum.

|       | `<s>` | `Humans` | `and` | `machines`| sum |
| ----------- | ----------- |-----------| -----|-----|---|
| `<s> Humans`   | 0       |  0 | 1 | 0 | 1|
| `Humans and`   | 0     | 0 | 0 | 1| 1|
## Probability of a Sequence
When calculating the probability of a sequence of words occurring together can be calculated using the [[Chain Rule]], since each word is interdependent on one another. Intuitively, the probability of a sequence is the conditional probability of each word, given the previous words in the sequence.
#### Approximation of Sequence Probability
However, this is limited by the fact that your corpus will likely not contain each sequence of words required to calculate all the products in the chain rule. As soon as one of the products is 0, the entire probability becomes 0.

We can approximate the probability by shortening the sequences in the conditional probabilities to a fixed length. For example, instead of looking at all the previous words in the sequence, we can just look at the previous word (i.e., the bi-gram). This approach, known as the Markov assumption, allows us to simplify the calculations and make them more computationally efficient.

So, instead of each probability being calculated as $P(w_{n}|w_{1}^{n-1})$ we can approximate it as $P(w_{n}|w_{n-N-1}^{n-1})$.
### Start and End Tokens
When using N-grams we are essentially sliding a window of size $N$ over the sequence. This becomes an issue at the start and end of a sequence, since we can't calculate the probability of the first $N-1$ words. To combat this, we can pre-process our corpus and add tokens to the start and end of the sequences in the corpus. 

For the start of a sequence, we can add $N-1$ start tokens (e.g., `<s>`), and for the end of a sentence we can just add a single end token (e.g., `</s>`). This also solves the issue where sequences of different lengths cannot be directly compared or processed by certain algorithms, known as the "variable-length sequence problem".
### Out of Vocabulary Words (OOV)
When using an [[Open Vocabulary]] it's possible to encounter words in a corpus which are not in your vocabulary. One way to deal with this is by replacing each of these instances with a tag, e.g., `<UNK>`. 

This should be used sparingly, since it can actually artificially increase your models apparent performance. For example, if half your corpus is now `<UNK>`, your model can assume that a series of `<UNK>` tokens has a high probability, even though it doesn't know what the actual words are.

### Smoothing
#### Laplacian Smoothing
If an N-gram is encountered which was not encountered in the corpus, it's count will be $0$, leading to the probability of the sequence being $0$. Laplacian or "Add-one" smoothing can reduce this effect by simply adding 1 to the numerator and $V$ to the denominator of the probability equation:
$$$P(w_{n}|w_{n-N+1}^{n-1}) = \frac{C(w_{n-N+1}^{n-1}, w_{n})+1}{C(w_{n-N+1}^{n-1}) + V}$$
Where:
 - $V$ is the size of the vocabulary.
#### Add-K Smoothing
For larger corpuses, "Add-k" smoothing can be used, which results in better smoothing.
#### "Stupid" Backoff
"Stupid" Backoff is a smoothing technique which works by using a smaller N-gram multiplied by a constant if the larger N-gram isn't found. I.e., if the N-gram is missing, use an N-1 gram. If that's also missing, use an N-2 gram, and so on.

Formally:
$$
\hat{P}(w_{n}|w_{n-2} w_{n-1}) = \lambda_{1} \times {P}(w_{n}|w_{n-2} w_{n-1}) + \lambda_{2} \times {P}(w_{n}| w_{n-1}) + \lambda_{3} \times {P}(w_{n})
$$
Where:
 - $\sum\limits_{i}\lambda_{i}=1$ 

