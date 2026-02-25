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
  $$\mathbb{E}[X(X-1)\cdots(X-k+1)] = G^{(k)}(1^{-}).$$
+ The variance of $X$ is given by
  $$\text{Var}(X) = G''(1^{-}) + G'(1^-)- [G'(1^-)]^2.$$
# Tricks
We may use [[root of unity filter]] in the following manner:

The probability that $X$ takes an even number is given by
$$\frac{G_{X}(1)+G_{X}(-1)}{2}.$$
The probability that $X$ takes a value that is divisible by $4$ is given by
$$\frac{G_{X}(1) + G_{X}(-1)+ G_{X}(i)+G_{X}(-i)}{4}.$$
# Also See:
+ [[the generating function of the sum of two random variables is the product of their generating functions]]
+ [[the expectation of a random variables is less than or equal to 1 iff its generating function has exactly one fixed point]]
