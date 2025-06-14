#flashcards

What are Hidden Markov Models (HMMs)?
?
Hidden Markov Models are statistical tools used to model and analyze systems observed indirectly, employing Markov Chains for underlying states and transitions.

What is the purpose of the transition matrix in an HMM?
?
The transition matrix in an HMM represents the probabilities of transitioning from one hidden state to another.

How are Hidden Markov Models used in Part of Speech Tagging?
?
HMMs assign the most likely part of speech to each word in a given sentence by modeling the sequences of words and their parts of speech.

What is the emission matrix in an HMM?
?
The emission matrix models the probabilities of observing a particular output given a hidden state, with rows representing states and columns representing observations.

What does each element of the emission matrix represent?
?
Each element of the emission matrix represents the probability of observing a particular output given a specific hidden state.

What is a key property of the rows of an emission matrix?
?
The row sum of each row in the emission matrix will always equal 1.

Why is it important that the row sums of the emission matrix equal 1?
?
It ensures that the probabilities of all possible observations from a given hidden state total to 1, maintaining the properties of a probability distribution.

Can you explain what Markov Chains are in the context of HMMs?
?
Markov Chains represent the underlying states of a system and the transitions between these states in Hidden Markov Models.

What role do probabilities play in Hidden Markov Models?
?
Probabilities in HMMs define the likelihood of transitioning between states and the likelihood of observing outputs from those states.

In what ways can Hidden Markov Models be applied outside of Part of Speech Tagging?
?
HMMs can be applied in various fields such as speech recognition, bioinformatics, and finance for sequence prediction and classification tasks.

