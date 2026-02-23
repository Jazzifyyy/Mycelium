---
tags:
  - college
  - stochastic_processes
  - info
---
# Definition
Suppose $X$ is a non-negative integer valued random variable. Then the generating function $P_{X}:(-1,1) \rightarrow \mathbb{R}$ is defined as
$$
\begin{align}
P_{X}(s) &= \sum_{n=0}^\infty \mathbb{P}(X=n)s^n \\
&= \mathbb{E}[s^X]
\end{align}$$
where $|s|<1$.

# Also See:
+ [[the generating function of the sum of two random variables is the product of their generating functions]]
+ [[the expectation of a random variables is less than or equal to 1 iff its generating function has exactly one fixed point]]
