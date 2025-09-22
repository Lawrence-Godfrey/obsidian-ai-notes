https://arxiv.org/pdf/2103.10385
https://huggingface.co/docs/peft/package_reference/p_tuning

Very similar to [[2021 - Prompt Tuning]].
## The Problem
Back in 2020–21, large pretrained LMs (like GPT-2/3, BERT, RoBERTa) were powerful but **adapting them to new tasks** was tricky:
- **Full fine-tuning**: update _all_ model parameters → very costly (hundreds of millions of parameters).
- **Discrete prompt engineering**: manually write natural language prompts (“The sentiment of this review is …”), but performance is brittle and highly sensitive to wording.
- **Prefix-/adapter-based methods**: early, but less well-established then.
## Discrete vs Continuous Prompts
- **Discrete prompts** = actual words/tokens you type in.  
    Example:
    `[CLS] The movie was great! [SEP] It was [MASK].`
    Here the discrete prompt is literally `"It was [MASK]"`.  
    Problem: these are limited by the model’s vocabulary and by our ability to guess good wordings.
- **Continuous prompts** = instead of fixed words, you learn a sequence of _embedding vectors_ that live in the model’s embedding space.    
    - Think of them as “soft tokens” that don’t correspond to any human-readable word.
    - These can represent much richer information and can be optimised by gradient descent.
    - They are prepended or inserted into the input sequence before passing it into the frozen model.
So P-Tuning replaces brittle hand-crafted _discrete_ prompts with trainable _continuous_ ones.
##  The Prompt Generator
In the paper, they don’t just learn arbitrary embeddings. They use a **prompt generator network** (often an LSTM or MLP) to map some task-specific signal (like the label space, input length, or task ID) into a sequence of continuous prompt embeddings.
- This allows flexibility:  
    Instead of one static learned prefix, you can generate **different continuous prompts for different inputs or tasks**.
- It makes the system more expressive than “prefix-tuning” (which just prepends a fixed set of learned vectors).
## How It Works (Pipeline)
1. Freeze the pretrained model (BERT/GPT).
2. Insert **M continuous prompt tokens** at certain positions (e.g. before the [CLS] token).
3. A small **prompt generator network** outputs embeddings for these prompt tokens.
4. Concatenate: `[prompt_embeddings] + [input_embeddings]`.
5. Pass this through the frozen LLM.
6. Only update the generator’s parameters (very lightweight).
### The _P-Tuning_ paper asked:
 - Can we **freeze the LLM** and only train a small, learnable _prompt embedding_ to adapt it to downstream tasks?
 - Discrete prompts suffer from instability (high variance), while P-Tuning stabilizes and improves performance.
 - Manual discrete prompts suffer from a large degree of instability.
 - Changing a single word in the prompt might result in substantial performance drop.
 - P-Tuning employs trainable continuous prompt embeddings in concatenation with discrete prompts.
 - Given a discrete prompt as the input, P-Tuning concatenates continuous prompt embeddings with the discrete prompt tokens and feeds them as the input to the language model. 
 - The continuous prompts are updated by backpropagation to optimize the task objective.
 - The intuition is that continuous prompts incorporate a certain degree of learnability into the input, which may learn to offset the effects of minor changes in discrete prompts to improve training stability.

![[Pasted image 20250910113202.png]]