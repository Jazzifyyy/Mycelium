---
tags:
  - info
  - college
  - stochastic_processes
---
# Definition
Suppose $\mathcal{T}$ is a countable set. Call it by the name *state space*. Then a sequence $\{ X_{n} \mid n \geq 0 \}$ is called a **markov chain** that takes values in $\mathcal{T}$ if
$$\mathbb{P}(\underset{}{x} = j \mid X_{n} =i, X_{n-1}=i_{n-1},\dots,X_{0}=i_{0}) = \mathbb{P}(X_{n+1}=j\mid X_{n} = i)$$