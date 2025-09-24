# Reconciling modern machine learning practice and the bias-variance trade-of
https://arxiv.org/pdf/1812.11118

 - One of the central tenets of machine learning, the bias-variance trade-off, appears to be at odds with the observed behaviour of methods used in the modern machine learning practice.
 - The bias-variance trade-off implies that a model should balance under-fitting and over-fitting. 
	 - In the modern practice, very rich models such as neural networks are trained to exactly fit (i.e., interpolate) the data. 
	 - Classically, such models would be considered over-fit, and yet they often obtain high accuracy on test data. 
- Traditionally we control model size to balance bias/variance:
	- If H is too small, all predictors in H may under-fit the training data and predict poorly on new data.
	- If H is too large, we may over-fit spurious patterns in the training data resulting in poor accuracy on new examples.
- In modern machine learning, we often use a large, over-parameterised model and fit it very closely to the training data (i.e., very low to no training loss), so that it "interpolates" the data, and find that it still generalises well. 

![[Pasted image 20250924091209.png]]
Classic U curve, which guides classical thinking, vs modern "double descent" curve, which subsumes the U curve. 

 - Choosing the smoothest function that perfectly fits observed data is a form of Occam’s razor: the simplest explanation compatible with the observations should be preferred.
 - By considering larger function classes, which contain more candidate predictors compatible with the data, we are able to find interpolating functions that have smaller norm and are thus “simpler”. Thus increasing function class capacity improves performance of classifiers

#### Classical regime (U-shape)
 - With too few parameters (underparameterised), the model can’t fit the data → high bias, high training/test error.    
    - As parameters increase, fit improves until you hit the “sweet spot.”
    - Just past that point, when model capacity is about equal to the number of data points (the _interpolation threshold_), the model is forced to fit noise/spurious patterns → test error spikes (classical overfitting).
#### Overparameterised regime (the second descent)
 - When you increase parameters _beyond_ the interpolation threshold, the model can find many different exact fits.    
    - Among these, optimisation procedures (like SGD) or inductive biases (e.g. favouring smoother, lower-norm solutions) tend to select “simpler” fits that generalise better.
    - As a result, test error drops again, often to below the classical “sweet spot”.

So the double descent curve merges the U-shape with this modern overparameterised phenomenon.