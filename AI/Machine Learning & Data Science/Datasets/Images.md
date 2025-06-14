# ImageNet
**Purpose**: A large-scale image classification benchmark.
**Size**: ~1.3 million images, 1,000 classes (ImageNet-1k).
**Resolution**: Images are of higher resolution.
**Use case**: Pretraining large models or benchmarking general image classification performance.
**Notes**: Also has a larger variant—**ImageNet-21k**—with 14 million images and 21,000 classes.
There are ImageNet Large Scale Visual Recognition Challenges (ILSVRC) which define "snapshots" of the dataset. I.e., the 
# CIFAR-100
**Purpose**: A small-scale benchmark for image classification.
**Size**: 60,000 images, 100 classes.
**Resolution**: 32x32 pixels.
**Use case**: Evaluating lightweight models or early-stage experimentation.
**Notes**: Due to its small image size and limited data, it's much easier to overfit.
CIFAR-10 has 60,000 images across 10 classes.
# VTAB (Visual Task Adaptation Benchmark)
**Purpose**: A benchmark for evaluating transfer learning across diverse visual tasks.
**Size**: 19 tasks from different domains; each task has only **1,000 training examples**.
**Task groups**:
- **Natural**: Everyday object classification (e.g., CIFAR, Pets, Flowers).
- **Specialized**: Medical/satellite imagery.
- **Structured**: Tasks requiring spatial/geometric understanding.
**Use case**: Evaluates a model's ability to generalize to new, low-data tasks.
**Notes**: Designed to stress-test few-shot and transfer learning capabilities.

# JFT-300M
**Type**: **Proprietary** dataset developed by Google.
**Size**: ~300 million high-resolution images.
**Labels**: ~18,000 classes (weakly supervised and noisy labels).
**Usage in ViT**:
- Used for **pretraining** the Vision Transformer at large scale.    
- Enables ViT models (especially ViT-H/14) to **outperform CNNs** like ResNet152x4 or EfficientNet on downstream tasks.
- Shows that **scale can compensate for lack of inductive bias** in pure transformers (i.e., no convolutional priors).
Also **JFT-3B**.


