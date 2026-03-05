---
tags:
  - info
  - college
  - statistical_methods
  - non_parametric
---
# Goal
Suppose $X_{1},\dots,X_{n}$ is a random sample from pdf $f$. We want to estimate the parameter $f$. 

(Note that $f$ is an infinite dimensional parameter.)

# Naive approach
We can estimate $f$ by a histogram. In such a case, we have the desirable properties: $\int \hat{f}(x)dx=1$ and $\hat{f} \geq 0$.

For any $t$, where 
$$x=:x_{i}< t< x_{i+1}:= x + \delta,$$
the estimate at $t$ is given by

$$\hat{f}(t)= \frac{\# (X_{i} \in (x, x + \delta))}{n \delta} = \frac{\hat{F}_{n}(x + \delta) - \hat{F}_{n}(x)}{\delta}$$

Problems: 
1. Histogram is not smooth
2. Location and width of the bins are subjective. 
