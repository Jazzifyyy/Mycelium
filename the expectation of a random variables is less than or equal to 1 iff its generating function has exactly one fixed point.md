---
tags:
  - college
  - stochastic_processes
  - info
---
# Statement
Suppose $X$ is a random variable such that $\mathbb{P}(X=1)<1$. Then its generating function $P$ has exactly one fixed point iff $\mathbb{E}[X] \leq 1$.
# Proof
**Case 1:**

Suppose that $1$ is the only fixed point, i.e., suppose that $P(s)>s$ on $[0,1)$. Then we have
$$\frac{1-P(s)}{1-s} <1$$
where $s \in [0,1)$. By the mean value theorem, there exists some $s < \sigma_{s}<1$ such that $P'(\sigma_{s})<1$.

Note that $s \uparrow 1 \implies \sigma_{s} \uparrow 1$. Thus, 
$$\lim_{ s \uparrow 1 }P'(\sigma_{s})=P'(1)=\mathbb{E}[X]\leq 1.$$
**Case 2:**

Suppose that there exists a fixed point $\sigma \in (0,1)$. (This is required only in case 2b.) 

**Case 2a:**

If $\mathbb{P}(X=0)=0$, then $P(0)=\mathbb{\mathbb{P}}(X=0)=0$. Thus, $0$ is another fixed point of $P$.

We don't consider the $\mathbb{P}(X=1)=1$ case since it is ruled out in the assumption. (Notice that, otherwise, if $\mathbb{P}(X=1)=1$, then $\mathbb{E}[X]=1$, even though $P$ has two fixed points.)

If $\mathbb{P}(X=1)<1$, then $\mathbb{P}(X=k)>0$ for some $k\geq 2$. Thus,
$$\begin{align}
\mathbb{E}[X] &= \sum_{k=1}^\infty k \mathbb{P}(X=k) \\
&= \mathbb{P}(X=1) + \sum_{j=2}^\infty \mathbb{P}(X=j) + \sum_{j=2}^\infty (j-1)\mathbb{P}(X=j) \\
&= 1 + \sum_{j=2}^\infty (j-1)\mathbb{P}(X=j) \\
&> 1 + 0=1. 
\end{align}$$
**Case 2b:**

Suppose $\mathbb{P}(X=0)>0$. Since $\sigma$ is a fixed point, we have $P(\sigma)=\sigma$. This yields
$$\frac{1-P(\sigma)}{1-\sigma}=1.$$
By the mean value theorem, there exists $\sigma<\tau<1$ such that 
$$P'(\tau)=1.$$
If we show that $P$ is strictly ...