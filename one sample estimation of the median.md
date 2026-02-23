---
tags:
  - college
  - statistical_methods
  - info
  - non_parametric
---
# Point estimate of the median
The point estimate of the population median is simply taken to be the sample median. 

Note that under non-parametric setup, judging the "quality" of an estimator is not easy.

# Confidence intervals
We also know from general inference that hypothesis tests can be inverted to get confidence intervals.

Suppose $\theta$ is the median and we have the problem
$$H_{0}: \theta= \theta_{0} \text{ v.s. }H_{a}: \theta \neq \theta_{0}.$$
Then 
$$Y= \#(X_{i}<\theta_{0}) \sim \text{Binomial}\left( n, \frac{1}{2} \right).$$
We do not reject $H_{0}$ if
$$c_{1}=\text{qbinom}(\alpha/2, n, 0.5) < Y < \text{qbinom}(1-\alpha/2, n, 0.5)=c_{2}.$$
Then note that
$$\begin{align}
1-\alpha &= \mathbb{P}(c_{1} < \#(X_{i}<\theta_{0}) < c_{2}) \\
&= \mathbb{P}(X_{(c_{1})} < \theta_{0}< X_{(c_{2})}).
\end{align}$$
# Example

The 2008-09 nine-month academic salary for Assistant Professors, Associate Professors and Professors in a college in the U.S.

```r
library(carData)
data("Salaries")
qbinom(0.025, 397, 0.5) #179
qbinom(0.975, 397, 0.5) #218
sort(Salaries$salary)[c(179,218)] #(105000, 111350)
```

Thus the confidence interval for the median salary is $(X_{(179)}, X_{(218)})$.