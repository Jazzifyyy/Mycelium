---
tags:
  - info
  - college
  - statistical_methods
  - non_parametric
---
# Definition
The Mann-Whitney U statistic is defined as
$$T^* = \sum_{i=1}^{n_{1}}\sum_{j=1}^{n_{j}}\mathbb{1}(X_{i}> Y_{j}).$$
# Properties
1. $T^*$ is the same as the statistic used in [[wilcoxon's rank sum test]], namely, 
   $$T = \sum_{i=1}^{n_{1}}R_{X_{i}} - \frac{n_{1}(n_{1}+1)}{2}.$$
   ### Proof
   We can write $T$ as follows:
$$T = \sum_{i=1}^{n_{1}}(R_{X_{i}} - i) = \sum_{i=1}^{n_{1}}(R_{X_{(i)}}-i)$$
where $X_{(1)}<\dots<X_{(n)}$. Now note that 
$$
\begin{align}
R_{X_{(i)}} &= \#(\text{obs} \leq X_{(i)}) \\
&= i + \#(Y < X_{(i)}).
\end{align}$$
By the above equation, we have
$$T = \sum_{i=1}^{n_{1}}\#(Y < X_{(i)}) = \sum_{i=1}^{n_{1}}\sum_{j=1}^{n_{j}}\mathbb{1}(Y_{j}< X_{i})$$
as required.
2. $T^*$ is the sum of $\mathbb{1}(X_{i}< Y_{j})$, which are unbiased estimators of $\theta = \mathbb{P}(X_{i}> Y_{j})$. 
   
   Also, $\mathbb{E}[T^*] = n_{1}n_{2}\theta$.