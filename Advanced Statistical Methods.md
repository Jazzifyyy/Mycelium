---
tags:
  - moc
  - college
---
### Non-parametric & distribution free methods

#### Motivation

1. To test if the mean of a population has a specified value in a null-hypothesis, we used the statistic $T=\frac{\bar{X} - \mu_{0}}{s/\sqrt{ n }}$. If $f \equiv \mathcal{N}$, then $T$ has a t-distribution. If not, for large values of $n$, we had the central limit theorem.
2. To test for the equality of means of two groups, we had two cases. If the distribution of the two groups were normal and were independent, then we had the two-sample t-test.
   Otherwise, for large number of samples, we had the central limit theorem.

We want to have alternate tests when the sample size is _small_ and the parent distribution is _unknown_. These tests shouldn't depend on any distribution and we do not assume any parametric model. 

#### The cost

If non-parametric models are so attractive, why not use it everywhere then?

If a parametric model is such that it is true to the real-world, then using that is "better" in the sense that, for hypothesis tests, both parametric and non-parametric tests will have the same level $\alpha$ but the former will have more power; and for hypothesis tests, the former will yield a narrower interval.

#### Tests
+ [[one sample median test - signed test]]
	+ [[one sample estimation of the median]]
+ [[wilcoxon's signed rank test]]
	+ [[example of performing the wilcoxon's signed rank test]]
+ [[wilcoxon's rank sum test]]
	+ This test uses the [[mann-whitney u statistic]]. 
	+ [[example of performing the wilcoxon's rank sum test]]
+ In a fully nonparametric setting, the difficulty with a “scale test” is that _scale is not intrinsically defined_: unlike in a parametric scale family (e.g., normal with variance $\sigma^2$), arbitrary distributions need not differ only by a multiplicative spread parameter. Without assuming a common shape, “more spread out” could reflect changes in skewness, tails, or location. The solution is to impose mild structural assumptions—such as equal medians, symmetry, or membership in a scale family—and then use rank-based procedures. See:
  [[fligner killeen test]].
+ [[kruskal wallis test for the equality of medians of multiple groups]]

# Problems
+ [[homework 1 problem 1 advanced statistical methods]]