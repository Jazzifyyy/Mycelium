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

# Shifted Histogram

We can estimate $f$ by a histogram. In such a case, we have the desirable properties: $\int \hat{f}(x)dx=1$ and $\hat{f} \geq 0$.

For any $t$, where 
$$x=:x_{i}< t< x_{i+1}:= x + \delta,$$
the estimate at $t$ is given by

$$\hat{f}(t)= \frac{\# (X_{i} \in (x, x + \delta))}{n \delta} = \frac{\hat{F}_{n}(x + \delta) - \hat{F}_{n}(x)}{\delta}.$$
Note that 
$$\hat{f}(t) \sim \frac{1}{n\delta}\text{Binomial}(n, F(x + \delta)-F(x)).$$
Denote $p:=F(x + \delta)-F(x)$.

Thus,
$$\mathbb{E}[\hat{f}(t)] = \frac{1}{n\delta}\cdot n(F(x + \delta)-F(x)) = \frac{F(x + \delta)- F(x)}{\delta}= \frac{p}{\delta}$$
and
$$\text{Var}(\hat{f}(t)) = \frac{1}{n^2 \delta^2}\cdot np(1-p) = \frac{p(1-p)}{n \delta^2}.$$

The mean squared error is given by
$$\text{MSE} = \text{Bias}^2 + \text{Var} = \left( \frac{p}{\delta} -f (t)\right)^2 + \frac{p(1-p)}{n\delta^2}.$$
Problems: 
1. Histogram is not smooth
2. Location and width of the bins are subjective. 

First problem solution:

We may minimize this expression over $\delta$ to get the optimal banwidth.

Second problem solution:

First note 

