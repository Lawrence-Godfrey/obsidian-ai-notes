Feature scaling is a technique used to normalise the range of the values of features in a dataset, which ensures that each feature contributes equally to the computation of the objective function. 

## Min-Max Scaling
Scale each feature to a given range, typically $[0, 1]$ or $[-1, 1]$ if negative values are present in the feature.
$$X_{scaled}= \frac{X - X_{min}}{X_{max}- X_{min}}$$
where 
 - $X$ is the original feature vector.
 - $X_{min}$ and $X_{max}$ are vectors of the min and max values of each feature.

## Mean Normalisation
Transforms features to have zero mean.
$$X_{scaled}= \frac{X - \mu}{X_{max}- X_{min}}$$
## Matrix Form
If you want to perform this scaling on the entire dataset at once, i.e., your $X$ is an $m\times n$ matrix where $m$ is the number of samples and $n$ is the number of features, then $X_{min}$ and $X_{max}$ need to be $m \times n$ matrices as well, where the columns will be the same min or max value repeated for a particular feature, and the rows will represent the different min/max values for the different features.
This matrix can be obtained by multiplying the transpose of $X_{min}$ or $X_{max}$ by a column vector of ones $1_m$, for example:
$$1_{n}X^T_{min}$$
