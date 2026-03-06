---
tags:
  - info
  - college
  - stochastic_processes
---
# Definition
Suppose $\mathcal{T}$ is a countable set. Call it by the name *state space*. Then a sequence $\{ X_{n} \mid n \geq 0 \}$ is called a **markov chain** that takes values in $\mathcal{T}$ if, for all $n \geq 0$, we have
$$\mathbb{P}(\underbrace{X_{n+1}= j}_{\text{future}}   \mid \underbrace{X_{n}= i}_{\text{present}}, \underbrace{X_{n-1}=i_{n-1},\dots,X_{0}=i_{0}}_{\text{past}}) = \mathbb{P}(X_{n+1}=j\mid X_{n} = i)$$
where $i,j, i_{n-1},\dots,i_{1},i_{0} \in \mathcal{T}$.

A markov chain is *homogeneous*, 