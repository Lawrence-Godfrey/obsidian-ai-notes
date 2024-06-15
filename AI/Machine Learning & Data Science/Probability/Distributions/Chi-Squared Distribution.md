The Chi-Squared Distribution is a type of [[Random Variables#Distributions|probability distribution]] which describes how the sum of the squares of a certain number of independent standard normal random variables (variables that follow the [[Normal Distribution]] with a mean of 0 and a standard deviation of 1) is distributed.

### Degrees of Freedom
The shape of the Chi-Squared distribution depends on a parameter called the “degrees of freedom” (df). The degrees of freedom usually represent the number of independent pieces of information you have after estimating one or more parameters.

For example, if you have a sample of 10 observations and you calculate the sample variance, you lose one degree of freedom because you used the sample mean in your calculation. So, you would have (10 - 1 = 9) degrees of freedom.

### Formula
If $( Z_1, Z_2, \ldots, Z_k )$ are independent [[Normal Distribution#Standard Normal Distribution|standard normal random variables]], then the sum of their squares:
$$
X = Z_1^2 + Z_2^2 + \cdots + Z_k^2
$$
follows a Chi-Squared distribution with  k  degrees of freedom.

![[Pasted image 20240529161256.png|centered]]

