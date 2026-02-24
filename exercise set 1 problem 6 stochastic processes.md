---
tags:
  - problem
  - stochastic_processes
  - college
---
# Problem
## Part b

A hen lays $N$ eggs, where $N \sim \text{Poisson}(\lambda)$. Each egg hatches with probability $p$ independently. Let $K$ be the number of chicks. Find the pgf of $K$ and identify its distribution.

# Solution
## Part b

Note that 
$$K = \sum_{i=1}^N \xi_{i}$$
where $\xi_{i}$ is $1$ if the egg hatches and is $0$ otherwise.


Note that the pgf of $N$ is
$$P_{N}(s)=e^{\lambda(s-1)}.$$


The pgf of $\xi$ is 
$$P_{\xi}(s) = 1-p + ps.$$

The pgf of $K$ is given by
$$
\begin{align}
P_{K}(s) &= P_{N}(P_{\xi}(s)) \\
&= e^{\lambda(1-p+ps-1)} \\
&= e^{\lambda p(s-1)}.
\end{align}
$$