---
tags:
  - info
  - college
  - stochastic_processes
---
# Definition

The probability generating function $G$ of a discrete random variable $X$ taking values in $\{ 0,1,2,\dots \}$ is defined as
$$G_{X}(s) = \mathbb{E}[s^X]= \sum_{k=0}^\infty \mathbb{P}(X=k)s^k. $$
# Properties
+ We have 
  $$\mathbb{P}(X=k) = \frac{G^{(k)}(0)}{k!}.$$
+ The expectation of $X$ is given by
  $$\mathbb{E}[X] = G'(1^-).$$
+ The $k$-th factorial moment of $X$ is given by
  $$\mathbb{E}[X(X-1)\cdots(X-k+1)] = G^{(k)}(1^{-1}).$$
+ The variance of $X$ is given by
  $$\text{Var}(X) = G''(1^{-}) + G'(1^-)- [G'(1^-)]^2.$$