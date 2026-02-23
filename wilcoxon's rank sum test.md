---
tags:
  - college
  - statistical_methods
  - info
  - non_parametric
---
# Setup and assumptions

Suppose $X_{1},\dots,X_{n_{1}} \overset{\text{iid}}{\sim}D_{1}$ and $Y_{1},\dots,Y_{n_{2}} \overset{\text{iid}}{\sim}D_{2}$.

Assumptions: 
1. The two samples are independent of each other.
2. $D_{1}$ and $D_{2}$ must be continuous.
3. $D_{1}$ and $D_{2}$ must have the same shape and scale.

Want to test (one sided):
$$H_{0}: D_{1} \text{ and }D_{2} \text{ are identical} \text{ v.s. }H_{a}: D_{1} \text{ is shifted left of }D_{2} \text{ or }D_{1} \text{ is shifted right of }D_{2}$$
Want to test (two sided):

$$H_{0}: D_{1} \text{ and }D_{2} \text{ are identical} \text{ v.s. }H_{a}: D_{1} \text{ is shifted left/right of }D_{2}$$
# Test procedure

1. Without loss of generality, let $n_{2}< n_{1}$. (i.e., the group with more samples are the $X$'s.)
2. Pool the sets together and rank them.
3. Determine the sum of ranks of the $X_{i}$'s in the pooled sample and denote it with $X$.
4. Define the test statistic $$T = X - \frac{n_{1}(n_{1}+1)}{2}.$$
   This is also known as the [[mann-whitney u statistic]].
5. The distribution of $T$ is then determined by permutation methods.

# Properties under the null hypothesis


Under the null hypothesis, $\theta= \mathbb{P}(X>Y)=\frac{1}{2}$. To understand why this must be true, note that, under the null, the distributions are same, and thus:
$$f_{X,Y}(x,y) = f_{X}(x)f_{Y}(y)=f_{X}(y)f_{Y}(x)=f_{X,Y}(y,x).$$
Thus, the joint pdf is symmetric about the line $y=x$. Thus,
$$\mathbb{P}((X,Y) \in\{ (x,y) | x<y \})=\mathbb{P}((X,Y) \in \{ (x,y) | x > y \}).$$
Therefore, $$\mathbb{P}(X<Y) = \mathbb{P}(Y<X)=\theta.$$
Now note that 
$$\begin{align}
1 &= \mathbb{P}(X>Y)+\mathbb{P}(X<Y) + \mathbb{P}(X=Y) \\
&= 2\theta + \mathbb{P}(X=Y) \\
\implies \theta &= \frac{1-\mathbb{P}(X=Y)}{2}.
\end{align}$$
Since the distribution is continuous, $\mathbb{P}(X=Y)=0$, and $\theta = \frac{1}{2}$.

Under the null, we have
$$\mathbb{E}[T^*] = \frac{n_{1}n_{2}}{2}$$
and
$$\text{Var}(T^*) = \frac{n_{1}n_{2}(n_{1}+n_{2}+1)}{12}.$$
(Variance expression was stated without proof.)

For moderately large $n_{1},n_{2}$, we have
$$\frac{T^* - \frac{n_{1}n_{2}}{2}}{\sqrt{ \frac{n_{1}n_{2}(n_{1}+n_{2}+1)}{12} }} \overset{d}{\rightarrow}\mathcal{N}(0,1).$$


# Also See:
+ [[example of performing the wilcoxon's rank sum test]]