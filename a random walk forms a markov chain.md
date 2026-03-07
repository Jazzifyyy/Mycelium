---
tags:
  - info
  - stochastic_processes
  - college
---
Consider a simple and symmetric random walk (See: [[random walk]]) in $\mathbb{Z}$ and denote the position of the walker at time $n$ is denoted by the random variable $S_{n}= S_{0} + \sum_{i=1}^n \epsilon_{i}$. 

Then $\{ S_{n} \mid n \geq 0 \}$ is a [[markov chain]].

Here, $\mathcal{T}=\{ -1,1 \}$, $\mathscr{T}= \mathbb{Z}$ and $f(i, \epsilon)=i+\epsilon$. Thus,
$$S_{n+1} = S_{0}  + \sum_{i=1}^{n+1}\epsilon_{i} = S_{0} + \sum_{i=1}^n \epsilon_{i} + \epsilon_{n+1} = S$$