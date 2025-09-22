https://arxiv.org/pdf/2104.08691
https://huggingface.co/docs/peft/en/package_reference/prompt_tuning

## Problem
Discrete / hard prompts are limited in terms of their improvements because they don't utilise backprop/end-to-end learning, are error-prone and require human involvement.

## Solution
Need a way to easily apply different learned prefixes to frozen models, for different tasks/users. 

![[Pasted image 20250920103926.png]]
The plot above shows that prompt tuning becomes more competitive with scale, closing the gap with T5 full finetuning at 10^10 parameters.

This paper introduces "prompt tuning", which can be seen as a simplification of [[2021 - Prefix Tuning]].

![[Pasted image 20250920105004.png]]

- Freezes the entire pre-trained model and only allows an additional k tunable tokens per downstream task to be prepended to the input text. 
 - This “soft prompt” is trained end-to-end and can condense the signal from a full labelled dataset, allowing our method to outperform few-shot prompts and close the quality gap with model tuning. 
 - At the same time, since a single pre-trained model is recycled for all downstream tasks, we retain the efficient serving benefits of frozen models.
 - This can also be seen as extreme regularisation, since most weights are frozen.
 - For embedding models, this doesn't affect the output embedding space, so backfilling of embedding stores isn't needed when prompt tuning.
 - Another benefit is that it completely avoids [[catastrophic forgetting]].

## Initialisation
 - The simplest is to train from scratch, using random initialisation. 
 - A more sophisticated option is to initialise each prompt token to an embedding drawn from the model’s vocabulary. 
	 - Conceptually, our soft-prompt modulates the frozen network’s behaviour in the same way as text preceding the input, so it follows that a word-like representation might serve as a good initialisation spot. 
 - For classification tasks, a third option is to initialise the prompt with embeddings that enumerate the output classes.
	 - Since we want the model to produce these tokens in the output, initialising the prompt with the embeddings of the valid target tokens should prime the model to restrict its output to the legal output classes.
