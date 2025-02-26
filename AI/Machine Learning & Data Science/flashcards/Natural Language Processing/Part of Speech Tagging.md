#flashcards

What is part of speech (POS) tagging?
?
POS tagging is a natural language processing technique that involves labeling words in a sentence with their corresponding part of speech category, such as noun, verb, or adjective.

How is POS tagging typically performed using Hidden Markov Models (HMM)?
?
POS tagging is performed by training a Hidden Markov Model on a corpus of labeled sentences, where the hidden states are the POS tags and the observations are the words in the sentences.

What is the purpose of the transition matrix in POS tagging with HMMs?
?
The transition matrix is used to calculate probabilities of transitioning from one POS tag to another based on counts of tag pairs in the training corpus.

What is the formula for calculating the transition probabilities in HMMs?
?
The transition probability is calculated as P(t_{i}|t_{i-1}) = C(t_{i-1}, t_{i}) / ∑ C(t_{i-1}, t_{j}) for all j.

How do we handle zero-value probabilities in the transition matrix?
?
We use a smoothing technique where we add a small value ε to the counts, resulting in the modified formula: P(t_{i}|t_{i-1}) = (C(t_{i-1}, t_{i}) + ε) / (∑ C(t_{i-1}, t_{j}) + N*ε).

What is the purpose of the emission matrix in HMMs for POS tagging?
?
The emission matrix calculates the probabilities of observing words given their corresponding POS tags.

What is the formula for calculating the emission probabilities in HMMs?
?
The emission probability is calculated as P(w_{i}|t_{i}) = (C(t_{i}, w_{i}) + ε) / (C(t_{i}) + N*ε).

What is the Viterbi Algorithm used for in the context of POS tagging?
?
The Viterbi Algorithm is used to calculate the most likely sequence of hidden states (POS tags) given a sequence of observations (words in a sentence).

What are the three main steps of the Viterbi Algorithm?
?
The three main steps are: 1) Initialization, 2) Forward Pass, and 3) Backward Pass / Traceback.

In the Viterbi algorithm, what is done in the initialization step?
?
The initialization step fills in the first column of the matrices C and D, representing the best probability so far for each state at the first observation.

How does the Forward Pass work in the Viterbi Algorithm?
?
For each subsequent observation and for each state, the algorithm computes the maximum probability of arriving at that state from any previous state and stores the value.

What is achieved during the Backward Pass in the Viterbi Algorithm?
?
The Backward Pass uses populated matrices C and D to produce the most likely sequence of states (POS tags) that generated the observed sequence, starting from the highest probability in the last column of matrix C.

