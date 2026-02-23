---
tags:
  - info
  - college
  - statistical_methods
---
For any distribution, the mean may not exist and hence the [[median]] is used.

Suppose $X_{1},\dots,X_{n} \overset{\text{iid}}{\sim}f$ where $\text{median}(X_{i}) = \theta$.

Assumptions:
1.  $f$ is a continuous distribution.

To test
$$H_{0}: \theta = \theta_{0} \text{ v.s. } H_{a}$$
define
$$Y_{i}:=\begin{cases}
1; \text{ if }X_{i} < \theta_{0} \\ \\
0; \text{ if }X_{i} \geq \theta_{0}.
\end{cases}$$

Note that since $X_{i}$'s are independent, $Y_{i}$'s would be independent, and under $H_{0}$, we will have
$$Y:= \sum_{i=1}^n Y_{i} \sim \text{Binomial}\left( n, \frac{1}{2} \right).$$
Observe that $Y$ is a statistic that counts the number of observations greater than or less than $\theta_{0}$ and is free of the original distribution!

The p-value is defined by
$$p= \mathbb{P}(Y\geq y)$$
where $y$ is the observed value of $Y$. 

Then we reject for significance level $\alpha$ if $\alpha \geq p$.

# Also See:
+ [[wilcoxon's signed rank test]]
+ we can invert this test to get confidence intervals for the median: [[one sample estimation of the median]]