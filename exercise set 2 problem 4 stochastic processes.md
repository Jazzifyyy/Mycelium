---
tags:
  - problem
  - stochastic_processes
  - college
---
# Problem 
Suppose $\{ Z_{n} \}$ is a branching process with $Z_{0}=1$ and with offspring mean $\mu$. 

1. Assume that $G''(1)< \infty$. Show that $\mathbb{E}[Z_{n}Z_{m}] = \mu^{n-m}\mathbb{E}[Z_{m}^2]$ for $m \leq n$. Hence find the correlation coefficient between $Z_{n}$ and $Z_{m}$ (in terms of $\mu$) for $m \leq n$.
2. Find $\mathbb{E}[Z_{n} | Z_{m} = k]$ for $m<n$ and $k\geq 0$.
# Solution
## Part 2

Given that $Z_{m}=k$, i.e., we have $k$ individuals in generation $m$, then
$$Z_{n}= \sum_{i=1}^k \mathcal{D}_{i}^{(n-m)}$$
where $D_{i}^{(n-m)}$ denotes the number of descendants of the $i$th individual after $n-m$ generations.

Thus, 
$$\mathbb{E}[Z_{n}|Z_{m}=k] = \mathbb{E}\left[ \sum_{i=1}^k \mathcal{D}_{i}^{(n-m)} \right]= \sum_{i=1}^k \mathbb{E}[\mathcal{D}_{i}^{(n-m)}] = \sum_{i=1}^k \mu^{n-m}=k\mu^{n-m}.$$
## Part 1

By the law of total expectation, 
$$\begin{align}
\mathbb{E}[Z_{n}Z_{m}] &= \mathbb{E}[\mathbb{E}(Z_{n}Z_{m}|Z_{m})] \\
&= \mathbb{E}[Z_{m}\mathbb{E}[Z_{n}|Z_{m}]] \\
&= \mathbb{E}[Z_{m}(Z_{m}\mu^{n-m})] \\
&= \mu^{n-m}\mathbb{E}[Z_{m}^2].
\end{align}$$