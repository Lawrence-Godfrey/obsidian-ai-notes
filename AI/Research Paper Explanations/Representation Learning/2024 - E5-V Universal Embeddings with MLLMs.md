https://arxiv.org/abs/2407.12580

![[Pasted image 20250706095945.png]]

The paper **"E5-V: Universal Embeddings with Multimodal Large Language Models"** introduces a framework called **E5-V**, designed to adapt **Multimodal Large Language Models (MLLMs)** for **universal multimodal embeddings**—representations that work well across text, images, and interleaved (composed) modalities.
## Motivation
Existing models like **CLIP** are good at aligning image and text pairs but:
- Struggle with interleaved inputs (e.g., composed image retrieval).
- Have weak language understanding (due to training on short captions).
- Require expensive and large-scale multimodal data for training.
## Core Idea: Use MLLMs Instead of CLIP
E5-V leverages MLLMs like **LLaVA-NeXT** that already fuse image and text. Instead of contrastive training on image-text pairs, E5-V:
- Uses **prompt-based representations** to map both modalities into the same semantic space.
- Trains **only on text pairs** (single modality), removing the need for visual encoders or multimodal data during training.
## Method
1. **Prompt Engineering**: Prompts like
    - `<image>\nSummary above image in one word:`
    - `<text>\nSummary above sentence in one word:`  
        guide the MLLM to embed content semantically (e.g., into “Plane” or “Flying”).
2. **Single Modality Contrastive Training**:
    - Trained on text-only datasets (e.g., NLI).
    - Optimises embeddings to distinguish between semantically similar/different sentences.
3. **Modality Gap Elimination**:
    - Visualisations show this prompt method unifies text and image embeddings without fine-tuning.
## Key Results (Zero-Shot, No Fine-Tuning on Evaluation Data)
- **Text-Image Retrieval**: Outperforms CLIP ViT-L and even matches EVA-CLIP 5B, despite not training on image-text pairs.
- **Composed Image Retrieval**: Beats state-of-the-art (e.g., iSEARLE-XL) on CIRR and FashionIQ datasets.
- **Image-Image Retrieval**: Embeds rendered text images much more accurately than baseline models.
- **Sentence Embeddings**: Matches or exceeds specialised LLM-based models like PromptEOL.
## Training Efficiency
- **95% lower training cost** compared to multimodal training.
- Single modality training: 1.5h on 32 V100 GPUs.
- Multimodal training: 34.9h on the same setup.
### Ablation Studies
- Confirm that the specific wording of prompts (especially “in one word:”) is crucial.
- Show that training on text pairs alone not only suffices but is better than image-text pairs for certain tasks.
## Zero-Shot Prompt Following
Even though E5-V was trained on static prompts, it generalises to follow **novel prompts** at inference (e.g., changing shirt styles in FashionIQ).

## What's actually being trained?
Only the **LLM component** of the MLLM is trained — the **visual encoder is removed** during training. So, it's effectively a **text encoder** being trained to produce embeddings that will also be used to embed **images at inference time**, via prompts.

---

## Input Format During Training
They use **text triplets** from Natural Language Inference (NLI) datasets:
- An anchor sentence: xix_ixi​
- A **positive** sentence with similar meaning: xi+x_i^+xi+​
- A **negative** sentence with different meaning: xi−x_i^-xi−​

They pass each sentence into a prompt like:
`<text> Summary above sentence in one word:`
and extract the **last token embedding** as the sentence’s representation​.

---

## Training Objective

They use **contrastive loss** (InfoNCE-style). So they're **just doing contrastive learning on text** using prompt-based embedding extraction.

---

## How does this help with multimodal inputs?
The trick is that **at inference**, they use **identically structured prompts for image inputs**, e.g.:

`<image> Summary above image in one word:`

The image gets passed through the frozen visual encoder and then the LLM, just like the text — and since the model was trained to align prompts like this in embedding space, the output embeddings **naturally align across modalities**.

> Think of it as: “Train the text encoder to embed meanings into token space. Then at inference, feed image features into the same prompt structure so the image is described in the same space.”

---

## TL;DR
- **Training**: Text in → prompt → LLM → last token embedding → contrastive learning
- **Inference**: Text _or_ image in → prompt → LLM → last token embedding → unified embedding space

They **never train on images**, but because the prompt structure at inference makes image inputs behave like text, the model generalises.

---
## Summary
**E5-V** is a **minimal, elegant, and surprisingly powerful** framework that rethinks multimodal training. By:
- Leveraging the semantic capabilities of MLLMs,
- Using clever prompts to unify modality representations,
- Training on text-only data,
it achieves **state-of-the-art multimodal performance**—efficiently, scalably, and flexibly.
Highly impactful paper.