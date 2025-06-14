https://arxiv.org/abs/2010.11929

- Currently, in vision, attention is either applied in conjunction with convolutional networks, or used to replace certain components of convolutional networks while keeping their overall structure in place. 
- This paper shows that this reliance on CNNs is not necessary
	- Pure transformer applied directly to sequences of image patches can perform very well on image classification tasks.
- Image patches are treated the same way as tokens (words) in an NLP application.
- Train the model on image classification in supervised fashion.
- When trained on the same amount of data as CNNs (ResNet), the ViT performs worse.
	- Less inductive bias, so worse on smaller datasets.
	- However, when training on much larger datasets, ViT outperforms ResNet models. 
		- 14M-300M Images ([[Images#JFT-300M|JFT-300]]).
	- Large scale training trumps inductive bias.
- [This paper](https://arxiv.org/abs/1911.03584) actually proposes a similar concept with 2x2 patches.
	- ViT only goes further by applying larger patches and using large scale pretraining.
- [iGPT](https://arxiv.org/html/2312.02147v2) pre-trained a model with low resolution images by predicting next pixels.

![[Screenshot from 2025-04-19 10-06-59.png]]

 - The original image ($x \in \mathbb{R} ^ {\text{Height} \times \text{width} \times \text{channels}}$ ) is converted into a sequence of flattened patches ($x \in \mathbb{R}^{\text{patches} \times (\text{patch resolution}^2 \times \text{channels})}$).
 - Patches are linearly projected to $x \in mathbb{R}^{D}$, where $D$ is the latent vector size used throughout the model.
 - Uses a `[class]` token like [[2018 - BERT|BERT]].
	 - This is just a $D$ dimensional embedding that is learned during training.
	 - It's randomly initialised and updated through backprop.
	 - During inference it is static.
	 - Essentially a token that asks "what is in this image?".
	 - It's output is essentially a **classifier-friendly representation** of the entire image.
	 - Selectively attends to most relevant patches, as opposed to using an MLP head, which treats all patch embeddings as equally important since it doesn't make use of attention. 
 - During **pre-training**
	 - They use a **multi-layer perceptron (MLP)** with one hidden layer as the classification head. So it's a two-layer neural network on top of the `[CLS]` token.
	 - They use 224x224 images, so you have a fixed sequence length.
	 - This means your positional embeddings can be learned and are static in length.
 - During **fine-tuning**
	 - They **remove** that MLP head and replace it with a new **single linear layer** that is trained on the downstream task (like ImageNet classification).
	 - They use higher-resolution images.
	 - Interpolate the positional embeddings to work with the higher resolution images.
		 - I.e., reshape the 1D set of 196 positional embeddings into 14x14 grid, then interpolate to higher resolution, and then convert back to a 1D set of embeddings. 
 - Uses learnable 1D positional embeddings.
	 - These are added to all patch embeddings, including `[class]` token.
 - MLP uses GELU activation.
	 - ![[Pasted image 20250419120558.png]]
 - 