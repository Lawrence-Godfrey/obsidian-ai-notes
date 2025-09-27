
# Few-Shot Parameter-Efficient Fine-Tuning is Better and Cheaper than In-Context Learning

https://arxiv.org/pdf/2205.05638

## Introduction
 - Introduces a new PEFT method called $(IA)^3$ that scales activations by learned vectors, attaining stronger performance while only introducing a relatively tiny amount of new parameters.
 - Also proposes a simple recipe based on the T0 model called T-Few that can be applied to new tasks without task-specific tuning or modifications.
 - ICL (In-Context Learning, i.e., few-shot prompting), has practical benefits, since adapting to different downstream tasks is easy and doesn't require any gradient-based training. 
	 - However, it requires processing a number of input-target pairs every time the model makes a prediction, incurring significant test-time compute costs.
	 - One way to reduce these costs is to cache the key and value vectors for the in-context examples, which are static. 
	 - In an extreme case, 32-shot ICL with 512 tokens per in-context example would result in over 144 gigabytes of cached key and value vectors for the GPT-3 model (32 examples × 512 tokens × 96 layers × 12288 dmodel × 32 bits each for the key and value vectors)
## T-Few Recipe
 - In this context, a recipe means a specific model and hyperparameter setting that provides strong performance on any new task without manual tuning or per-task adjustments.
 - the T-Few recipe is defined as follows:
	 - T0 model as a backbone. 
	 - Add (IA)3 for downstream task adaptation and use parameters initialised from pre-training (IA)3 on the same multitask mixture for T0. 
	 - As an objective, use the sum of a standard language modelling loss LLM, an unlikelihood loss $L_{UL}$ for incorrect choices, and a length-normalised loss $L_{LN}$. 
	 - Train for 1,000 steps with a batch size of 8 sequences using the Adafactor optimizer with a learning rate of $3e −3$ and a linear decay schedule with a 60-step warmup. 
	 - Apply prompt templates to downstream datasets during training and inference to convert each example into an instructive text-to-text format. 
	 - Apply this recipe to every downstream dataset in exactly the same way without per-dataset hyperparameter tuning or modifications. This makes the recipe a realistic option for few-shot learning settings where validation sets are tiny by definition


![[Pasted image 20250926080524.png]]

## IA3
 - "Infused Adapter by Inhibiting and Amplifying Inner Activations"
 - Prompt tuning and prefix tuning methods work by concatenating learned vectors to activation or embedding sequences and are therefore examples of activation-modifying PEFT methods that allow for mixed-task batches. 
	 - However, these do not have the same accuracy improvements as other non-mixed-task performant PEFT methods.
 - IA3 uses element-wise multiplication (i.e. rescaling) of the model’s activations against a learned vector.
 - $l \odot x$ where $l ∈ R^d$ is a learned task-specific vector, $odot$ represents element-wise multiplication, and $x ∈ R^{T\times d}$ is a length-T sequence of activations.
 - Experiments found it was not necessary to introduce a learned rescaling vector for each set of activations in the Transformer model. 
	 - Instead, they found it was sufficient to introduce rescaling vectors on the keys and values in self-attention and encoder-decoder attention mechanisms and on the intermediate activation of the position-wise feed-forward networks.
 - Therefore, they introduce three learned vectors, $l_k$, $l_v$ and $l_{ff}$ (feed-forward), which are incorporated into the softmax function like this:
$$
\text{softmax}\!\left(\frac{Q \,(l_k \odot K^{T})}{\sqrt{d_k}}\right)\,(l_v \odot V)
$$
 - In the position-wise feed-forward networks:
$$
(l_{ff} \odot \gamma(W_1 x)) W_2
$$
		where $\gamma$ is the feed-forward network non-linearity. 
	
 - A separate set of $l_k$, $l_v$, and $l_{ff}$ vectors in each Transformer layer block. 
	 - This adds a total of $L(d_k + d_v + d_{ff})$ new parameters for a L-layer-block Transformer encoder and $L(2d_k + 2d_v + d_{ff})$ (with factors of 2 accounting for the presence of both self-attention and encoder-decoder attention) for a L-layer-block decoder. 
	 - $l_k$, $l_v$, and $l_{ff}$ are all initialised with ones so that the overall function computed by the model does not change when they are added. 
 - These vectors an be "pushed down" into the model for single-task models, incurring no additional inference costs.

![[Pasted image 20250927094303.png]]