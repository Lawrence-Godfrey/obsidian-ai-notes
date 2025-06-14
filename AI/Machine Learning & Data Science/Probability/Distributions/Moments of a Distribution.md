The moments of a distribution are measures that provide useful insights about the characteristics of the distribution. 

The first moment of a distribution is the [[AI/Machine Learning & Data Science/Probability/Basics#Expected Value|mean]]
the second, $E[X^2] - (E[X])^2$ is the [[AI/Machine Learning & Data Science/Probability/Basics#Variance|variance]] (about the origin)
the third, $E[(X−E[X])^3]$ is the [[Skewness]] 
and the fourth, $E[(X-E[X])^4] - 3(E[(X-E[X])^2])^2$ is the [[Kurtosis]].

In general, the $kth$ moment can be described by
$$
E[X^k] - \sum_{i=1}^{k-1} C(k, i)E[X^i]E[X]^{k-i}
$$
where $C(k, i)$ is the binomial coefficient.