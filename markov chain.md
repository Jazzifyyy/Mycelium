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

A markov chain is *homogeneous*, if $\mathbb{P}(X_{n+1}=j\mid X_{n} = i)$  does not depend on $n$, i.e.,
$$\mathbb{P}(X_{n+1}=j\mid X_{n} = i) = \mathbb{P}(X_{1}=j \mid X_{0}=1)$$
for $n \geq 1$.

# Notation and naming conventions
Define $p_{ij}:= \mathbb{P}(X_{n+1} = j \mid X_{n} = i) = \mathbb{P}(X_{1}=j \mid X_{0}=i)$.

Note that
$$\sum_{j \in \mathcal{T}} p_{ij} = \sum_{j \in \mathcal{T}}\mathbb{P}(X_{1}=j \mid X_{0}=i)= \mathbb{P}\left( \bigcup_{j \in \mathcal{T}}\left\{  X_{1}=j  \right\}  {\bigg |} X_{0}=i\right)=1.$$
Define $P := ((p_{ij}))_{\mathcal{T} \times \mathcal{T}}$ and call it the *transition probability matrix*.

Note that 
$$P \cdot\mathbf{1}^T= \mathbf{1}^T,$$
i.e., $\mathbf{1}^T$ is an eigenvector corresponding to the eigenvalue $1$.

The distribution of $X_{0}$ is called the **initial distribution**.

# A sequence of rv is a markov chain when?
Let $\{ X_{n} \mid n \geq 0 \}$ be a sequence of random variables that takes values in $\mathcal{T}$ and $X_{0} \sim \mu$. Let $\{ \xi_{n} \mid n \geq 1 \}$ be a sequence of iid random variables, all of them being independent of $X_{0}$, that also takes values in $\mathcal{T}$.


