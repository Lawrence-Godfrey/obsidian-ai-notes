#flashcards

What are adversarial attacks?
?
Techniques used to manipulate input data to machine learning models, particularly deep neural networks, resulting in incorrect predictions or classifications.

What is an adversarial example?
?
Manipulated input data that has been altered in a subtle way to cause a model to make an incorrect prediction.

What is the significance of imperceptibility in adversarial attacks?
?
The changes made to the input are often so small that they go unnoticed by humans yet can drastically alter a model's output.

What does transferability mean in the context of adversarial attacks?
?
Adversarial examples generated for one model can sometimes deceive other models, regardless of differences in architecture or training data.

What are the potential impacts of adversarial attacks?
?
They raise concerns about the robustness and trustworthiness of machine learning models in critical applications such as medical imaging and autonomous driving.

Define white-box attacks.
?
Attacks where the attacker has full knowledge of the model, including its architecture, parameters, and training data, allowing them to create targeted adversarial examples.

Define black-box attacks.
?
Attacks where the attacker has limited knowledge of the model, enabling them to generate adversarial examples, often through the creation of surrogate models.
<!--SR:!2025-02-19,3,250-->

What is a targeted adversarial attack?
?
An attack aimed at making a model produce a specific incorrect output.

What is an untargeted adversarial attack?
?
An attack aimed at causing the model to produce any incorrect output.

What is the Fast Gradient Sign Method (FGSM)?
?
A method for crafting adversarial examples that involves adding a small fraction of the sign of the gradient of the loss concerning the input data to the original input.

Describe the DeepFool method for generating adversarial examples.
?
An iterative method that perturbs the input to cross the decision boundary of the model.

What is the Jacobians-based Saliency Map Attack (JSMA)?
?
A method that focuses on a small subset of input features to modify them based on the Jacobian matrix of the model's output concerning its input.

What is adversarial training?
?
A defense mechanism that incorporates adversarial examples into the training data to enhance model robustness against such inputs.

What is model ensembling?
?
Using a collection of models to make predictions, thereby reducing the risk of adversarial examples impacting the predictions.

How can input preprocessing defend against adversarial attacks?
?
By transforming input data through methods like denoising or quantization to lessen the effects of adversarial perturbations.

What is gradient masking or obfuscation in the context of adversarial defenses?
?
Altering the model or its training process to make it difficult for attackers to compute meaningful gradients for crafting adversarial examples.

Why is the arms race between adversarial attacks and defenses ongoing?
?
Many proposed defenses have been shown to be ineffective against more sophisticated or adaptive attacks, leading to continuous research in both areas.

