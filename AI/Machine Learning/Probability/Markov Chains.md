Markov Chains is a stochastic model which describes a sequence of possible events. To get the probability of an event it needs only the state of the previous event. In computer science, a Markov Chain can be represented as a directed graph:

![[Pasted image 20231008195522.png]]

### Transition Matrix
The graph can also be represented as a transition matrix, where the rows $q_{1}, q_{2}, ... q_{N}$ represent the current state, and the columns $q_{1}, q_{2}, ... q_{N}$ represent the target state. Each element in the table stores the probability of transitioning from the current state to the given target state. 

### Initial State
In the case that there is no previous state to look at, you can add an initial state $\pi$, which will be represented by the first row of the transition matrix.