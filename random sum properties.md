---
tags:
  - college
  - stochastic_processes
  - info
---
# Setup
Suppose $\{ X_{i} \}$ is a sequence of iid non-negative random variables with $P$ being their generating function.  

Suppose $N$ is another random variable (that is independent of the $X$'s) with $G$ being its generating function.

Define the random sum:
$$S_{N} = \begin{cases}
0 ; \text{ if }N=0 \\
\sum_{i=1}^N X_{i}; \text{ if }N\geq 1.
\end{cases}$$
# Exploration
The generating function of $S_{N}$ is given by
$$\begin{align}
\mathbb{E}[s^{S_{N}}] &= \mathbb{E}\left[ s^{S_{N}} \sum_{n=0}^\infty\mathbb{1}(N=n) \right] \\
&= \sum_{n=0}^\infty \mathbb{E}[s^{S_{N}}. \mathbb{1}(N=n)] \\
&= \mathbb{E}[\mathbb{1}(N=0)] + \sum_{n=1}^\infty \mathbb{E}[s^{X_{1}+\dots+X_{n}}.\mathbb{1}(N=n)] \\
&= \mathbb{P}(N=0) + \sum_{n=1}^\infty \mathbb{E}[s^{X_{1}+\dots+ X_{n}}].\mathbb{E}[\mathbb{1}(N=n)] \\
&= \mathbb{P}(N=0) + \sum_{n=1}^\infty [P(s)]^n \mathbb{P}(N=n) \\
&= G(P(s)).
\end{align}$$
Thus,
$$P_{S_{N}}(s) = G(P(s)) \implies P'_{S_{N}}(s) = G'(P(s)).P'(s).$$
Let $s \uparrow 1$ to get
$$\mathbb{E}[S_{N}] = \mathbb{E}[N]\cdot\mathbb{E}[X_{i}].$$
