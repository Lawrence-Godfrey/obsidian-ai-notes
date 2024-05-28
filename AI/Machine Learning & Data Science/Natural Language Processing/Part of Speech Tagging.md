Part of speech (POS) tagging is a natural language processing technique that involves labelling words in a sentence with their corresponding part of speech category, such as noun, verb, adjective, etc.
### Hidden Markov Models
POS tagging can be done by training a [[Hidden Markov Model]] (HMM) on a corpus of labeled sentences. In this case the hidden states are the POS tags, and the observations are the words in the sentences.
#### Transition Matrix
Training the HMM involves counting the occurrence of each tag pair $C(t_{i-1}, t_{i})$ in the corpus and dividing that by that count by the total number of times tag $t_{i-1}$ appears in the corpus:
$$ P(t_{i}|t_{i-1}) = \frac{C(t_{i-1}, t_{i})}{\sum\limits_{j=1}^{N}C(t_{i-1}, t_{j})}$$
This will produce the transition matrix used to calculate probabilities from going from one POS tag to another. In order to accommodate the start of a sentence, a `<s>` tag can be added to the start of the sentence. This is used to calculate the initial probability $\pi$ in the transition matrix.
#### Smoothing
Since it is possible to have combinations of tags which don't occur in the corpus, which results in zero-value probabilities, the following formula can be used instead, which smooths the probability.
$$P(t_{i}|t_{i-1}) = \frac{C(t_{i-1}, t_{i}) + \epsilon}{\sum\limits_{j=1}^{N}C(t_{i-1}, t_{j}) + N*\epsilon}$$
#### Emission Matrix
Calculating the emission matrix is fairly similar to the transition matrix. We now count the number of occurrences of a word $w_{i}$ being tagged with a given POS tag $t_{i}$ divided by the number of occurrences of that tag in the corpus:
$$
P(w_{i}|t_{i-1}) = \frac{C(t_{i}, w_{i}) + \epsilon}{\sum\limits_{j=1}^{V}C(t_{i}, w_{j}) + N*\epsilon}

$$
$$
= \frac{C(t_{i}, w_{i}) + \epsilon}{C(t_{i}) + N*\epsilon}
$$
### The Viterbi Algorithm
**Video**: [The Viterbi Algorithm : Natural Language Processing](https://www.youtube.com/watch?v=IqXdjdOgXPM)

The [[Viterbi Algorithm]] can be used to calculate the most likely sequence of hidden states (POS tags) given a sequence of observations, i.e., a sentence. This involves iteratively calculating the probability of each possible state sequence and selecting the one with the highest probability. Since a given observation (word) may be emitted from multiple hidden states, each possible path from the current state to each observation needs to be calculated.

The algorithm can be broken down into 3 steps:
1. **Initialisation**: In the initialisation step we initialise two matrices $C$ and $D$. These matrices have the sequence of tokens or words as the columns, and the POS tags as rows, and represent the best probability so far for each state at each observation and which state we came from to get that probability respectively. For initialisation we only fill in the first column of these matrices.
2. **Forward Pass**: For each subsequent observation and for each state, compute the maximum probability of arriving at that state from any previous state, and store the value.
3. **Backward Pass / Traceback**: The matrices $C$ and $D$ are now populated. These can now be used to produce a sequence of states (POS tags) which most likely generated this sequence. We start at the end of the $C$ matrix and find the highest probability of that column, i.e., the highest probability for the last word in the sequence. The corresponding element in matrix $D$ represents the state of the previous word in the sentence. Now simply use the value in matrix $D$ for the previous word to do the same, and go back through the sequence until you get to the start, keeping track of each state along the way.