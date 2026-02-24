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
+ 