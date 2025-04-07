https://arxiv.org/pdf/1706.03762
## Problem
- The main problem being solved by Transformers is the inherently sequential nature of previous sequence modelling techniques like RRNs/LSTMs.
	- These techniques had 3 main issues: Long-range dependencies, limited ability to parallelise and vanishing/exploding gradients.
	- **Long-range dependencies**: Information has to propagate sequentially through hidden states. This makes it harder to capture dependencies between distant tokens because signals weaken over time.
	- **Lack of Parallelisation**: Since each step depends on the previous one, the model must process data sequentially, which limits parallel execution.
	- **Vanishing/exploding Gradients**: Because gradients have to back-propagate through time, the longer the sequence, the more multiplications in your chain-rule. Gradients below 1 will iteratively get smaller and gradients above 1 will iteratively get bigger.
- The Transformer allows for significantly more parallelisation and reached new state of the art in translation quality after being trained for as little as twelve hours on eight P100 GPUs.
- The Extended Neural GPU, ByteNet and ConvS2S all attempted to solve the sequential computation problem.
	- However, they use convolutions, meaning the computation required to relate signals grows with distance. 
	- Transformers relate inputs using a constant number of operations.
		- This does reduce effective resolution, which they counteract using multiple attention heads.
- Self-attention/intra-attention relates different positions of a single sequence. 
	- **End-to-End Memory Networks (MemNets)** used a type of iterative attention mechanism, where inputs were repeatedly attended to stored memory slots. These memory slots carried relevant information. 
		- However, this means inputs are being attended to static memory units. 
	- Self-attention is dynamic. The attention depends on the input, rather than static memory. 
## Architecture
![[Pasted image 20250327130452.png]]

- 2 Macro blocks in this architecture:
	- **Encoder**: Converts the input sequence into a representation.
	- **Decoder**: Uses the input sequence representation and the current (previous) outputs to produce the probability distribution over next tokens in the output sequence. 
- Input token sequences are embedded with a learned word embedder, producing vectors of size $d_{model}$ (512 in this paper).
- **Positional encodings** are added to the embeddings to encode positional information.
	- A set of $sin$ and $cos$ functions are used to create a vector of size $d_{model}$.
	- The idea is that the periodic functions have decreasing wavelengths.
	- The higher wavelengths capture global distance of the input sequences while the lower ones capture more local distances.
	- This was compared to using learned positional encodings but the results were very similar.
### Attention Mechanism
![[Pasted image 20250329103858.png]]

- Attention works with a set of weight matrices which transform the input embeddings into 3 different representations: **Keys**, **Values** and **Queries**, each of size $(d_{model}​,d_{model}​)$. $$Q=XW_Q​,K=XW_K​,V=XW_V​$$
- Intuitively, the values contain important information from the input sequence, the keys allow those values to be retrieved, and the queries know what needs to be retrieved using the keys and values. 
- The output of the attention block is an **attention weight matrix** of shape $(T, T)$, where each token attends to all tokens (including itself).
- In **multi-head attention**, the $K$, $V$ and $Q$ matrices are split into sub-matrices and each fed into an attention head. This allows each head learns to focus on different relationships (e.g., syntactic vs. semantic dependencies).
- The result of the first **MatMul** between $Q$ and $K$ is scaled to reverse the effect of the dot-product between high-dimensional matrices and the **SoftMax** function which further pushes these values. This is done by dividing by $\sqrt{d_k}$.
	- $d_{k}$ is the dimensionality of the keys vector. This is determined by the model dimensionality $d_{model}$ and number of heads: $d_{k}​=\frac{h} {d_{model}​​}$.

![[Pasted image 20250329105840.png]]

- Note that according to this table, RNNs should actually have less complexity when $n > d$. In today's world with sequence lengths of thousands of tokens, shouldn't RRNs be way more efficient? 
	- Technically, RNNs have better **asymptotic complexity**, but they are **sequential**, making them much slower in real-world implementations.
	- Instead of reverting to RNNs, modern models **optimise self-attention** using sparse approximations or locality-sensitive hashing.

![[Pasted image 20250329162913.png]]




![[Pasted image 20250330112408.png]]