https://arxiv.org/abs/2304.08485

## Problem
Instruction tuning large language models (LLMs) using machine-generated instruction-following data has been shown to improve zero-shot capabilities on new tasks, but the idea is less explored in the multimodal field.
## Solution
Introduces **LLaVA**: Large Language and Vision Assistant, an end-to-end trained
large multimodal model that connects a vision encoder and an LLM for general-purpose visual and language understanding.
 - Uses language-only GPT-4 to generate multimodal language-image instruction-following data.
 - Visual Instruction-Tuning: The first attempt to extend instruction-tuning to the language-image multimodal space.
	 - Previous models which utilise machine-generated instruction-following samples: Alpaca, Vicuna, GPT-4-LLM (all text-only).
	 - Convert image-text pairs into an appropriate instruction-following format, using ChatGPT/GPT-4.
	 - Connects the visual encoder of CLIP with the language decoder Vicuna.
		 - Fine-tune end-to-end on generated instruction-following data. 
 - 158K unique language-image instruction-following samples in total.
	 - 58K conversations,
	 - 23K detailed description,
	 - and 77k in complex reasoning.

 ![[Pasted image 20250616144744.png]]
 - Uses Vicuna as the language model, and the pre-trained CLIP visual encoder ViT-L/14. 
 - Trainable projection matrix $W$ to convert $Z_v$ into language embedding tokens $H_v$ , which have the same dimensionality as the word embedding space in the language model.

![[Pasted image 20250622153205.png]]
 - Example input sequence for training.
 - Only the **Assistant** responses and `<STOP>` tokens (green) are used to calculate loss.

### Two-Stage Training Approach
 - **Stage 1** - Visual and language transformers are frozen, and only the projection $W$ is trained. This aligns the visual features with the word embeddings.
 - **Stage 2** - End-to-end fine-tuning. Visual encoder is frozen, and the projection layer and LLM is fine-tuned end-to-end on instruction-following data.


