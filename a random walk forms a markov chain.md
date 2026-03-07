---
tags:
  - info
  - stochastic_processes
  - college
---
Consider a simple and symmetric random walk (See: [[random walk]]) in $\mathbb{Z}$ and denote the position of the walker at time $n$ is denoted by the random variable $S_{n}= S_{0} + \sum_{i=1}^n \epsilon_{i}$. 

Here, $\mathcal{T}=\{ -1,1 \}$, $\mathscr{T}= \mathbb{Z}$ and $f(i, \epsilon)=i+\epsilon$. Thus,
$$S_{n+1} = S_{0}  + \sum_{i=1}^{n+1}\epsilon_{i} = S_{0} + \sum_{i=1}^n \epsilon_{i} + \epsilon_{n+1} = S_{n} + \epsilon_{n+1}=f(S_{n}, \epsilon_{n+1}).$$

Then $\{ S_{n} \mid n \geq 0 \}$ is a [[markov chain]]. (See: [[markov chain#A sequence of rv is a markov chain when?]])

Note that
$$
\begin{align}
p_{ij} &= \mathbb{P}(S_{n+1}=j \mid S_{n}=i) \\
&= \mathbb{P}(f(i, \xi_{1})=j) \\
&= \mathbb{P}(i + \epsilon_{i} = j) \\
&= \mathbb{P}(\epsilon_{i} = j -i) \\
&= \begin{cases}
\frac{1}{2}; \text{ if }j= i+1\text{ or }j = i -1 \\
0; \text{ otherwise}.
\end{cases}
\end{align}
$$

