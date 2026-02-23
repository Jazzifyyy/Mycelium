---
tags:
  - problem
  - college
  - stochastic_processes
---
# Problem 
## Part a

Find the extinction probability $\rho$ for a branching process with offspring distribution:
1. $\mathbb{P}(\xi=0)=\frac{2}{3}$, $\mathbb{P}(\xi=3)=\frac{1}{3}$.
2. $\mathbb{P}(\xi=0)=\frac{1}{2}$, $\mathbb{P}(\xi=1)=\mathbb{P}(\xi=3)=\frac{1}{4}$.
## Part b

Consider a branching process where each individual has a random number of offspring with a $\text{Poisson}(\lambda)$ distribution. Determine the critical value $\lambda_{c}$ below which the branching process becomes extinct with probability $1$. Find the extinction probability $\rho$ for $\lambda > \lambda_{c}$.
# Solution
## Part a

Note that in both the cases, we have $\mathbb{E}[\xi]=1\leq 1$. Thus $\rho=1$.

## Part b

We have $\xi \sim \text{Poisson}(\lambda)$ and $\mathbb{E}[\xi]=\lambda$. Note that if $\lambda \leq 1$, then $\rho =1$ and if $\lambda > 1$, then $\rho < 1$. Thus the critical value is $\lambda_{c}=1$.

For $\lambda>\lambda_{c}=1$, the extinction probability is the solution of $\rho=G(\rho)$:
$$\begin{align}
\rho &= \sum_{k=0}^\infty \mathbb{P}(\xi=k)\rho^k \\
&= \sum_{k=0}^\infty \frac{e^{-\lambda}\lambda^k}{k!}\rho^k \\
&= e^{-\lambda}\sum_{k=0}^\infty \frac{(\rho \lambda)^k}{k!} \\
&= e^{-\lambda}e^{\lambda \rho} \\
&= e^{\lambda(\rho-1)}.
\end{align}$$