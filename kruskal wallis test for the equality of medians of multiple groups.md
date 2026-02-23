---
tags:
  - info
  - non_parametric
  - statistical_methods
  - college
---
# Setup and assumptions
We have
$$\begin{align}
X_{11},\dots,X_{1n_{1}} &\overset{\text{iid}}\sim F_{1} \\
&\vdots \\
X_{m1},\dots,X_{mn_{m}} &\overset{\text{iid}}\sim F_{m}.
\end{align}$$
Assumptions:
+ All the samples are independent of each other.
+ $F_{1},\dots,F_{m}$ must have the same shape and scale.
+ For simplicity, assume no ties.

To test:

The null hypothesis is that the medians of all groups are equal, and the alternative hypothesis is that at least one population median of one group is different from the population median of at least one other group.

# Motivation

Under the null, we expect no difference in the average ranks of the groups, i.e., we expect $\frac{R_{j}}{n_{j}}$ to be same for $j \in \{ 1,\dots,m \}$. So all we need to do here is to check how "spread out" the values are, by using a statistic which resembles a "sum of squares between" expression. 

(Note that in a SSB expression, we have a multiplicative factor of $n_{i}$ to weight each group's deviation based on its sample size. If one group has 2 people and another has 50, a deviation of 5 points from the grand mean in the larger group is far more significant to the total variance than a 5-point deviation in the smaller group.)
# Procedure
1. Pool all the $X_{ij}$'s together and rank them. Sum the ranks of $X$'s in sample $j$ to get $R_{j}$ where $j = 1,\dots,m$.
2. Define $\bar{R}=\frac{n(n+1)}{2n} = \frac{n+1}{2}$ as the average of all the ranks. Now define the test statistic
   $$\begin{align}
T &= C\sum_{j=1}^m n_{j}\left( \frac{R_{j}}{n_{j}} - \bar{R} \right)^2 \\
&= C\sum_{j=1}^m n_{j}\left( \frac{R_{j} - n_{j} \bar{R}}{n_{j}} \right)^2 \\
&= C\sum_{j=1}^m \frac{R_{j}^2 + n_{j}^2\bar{R}^2 - 2R_{j}n_{j}\bar{R}}{n_{j}} \\
&= C\left[ \frac{(n+1)^2n}{4}- \frac{(n+1)^2n}{2} +\sum_{j=1}^m \frac{R^2_{j}}{n_{j}} \right] \\
&= C\left[ \sum_{j=1}^m \frac{R_{j}^2}{n_{j}} - \frac{(n+1)^2n}{4} \right]
\end{align}$$
where $C = \frac{12}{n(n+1)}$; this is to ensure that $T$ is approximate a chi-squared distribution. Upon further simplification, we have
$$T = \frac{12}{n(n+1)} \sum_{j=1}^m \frac{R_{j}^2}{n_{j}} - 3(n+ 1).$$
3. $T$ is approximately a $\chi^2_{m-1}$ where $n_{j}$ is moderately large for each $j$.
4. The exact distribution of $T$ can also be found using permutation methods. 

