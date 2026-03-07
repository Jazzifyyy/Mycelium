---
tags:
  - info
  - college
  - stochastic_processes
---
# Definition
Suppose $\mathcal{T}$ is a countable set. Call it by the name *state space*. Then a sequence $\{ X_{n} \mid n \geq 0 \}$ is called a **markov chain** that takes values in $\mathscr{T}$ if, for all $n \geq 0$, we have
$$\mathbb{P}(\underbrace{X_{n+1}= j}_{\text{future}}   \mid \underbrace{X_{n}= i}_{\text{present}}, \underbrace{X_{n-1}=i_{n-1},\dots,X_{0}=i_{0}}_{\text{past}}) = \mathbb{P}(X_{n+1}=j\mid X_{n} = i)$$
where $i,j, i_{n-1},\dots,i_{1},i_{0} \in \mathscr{T}$.

A markov chain is *homogeneous*, if $\mathbb{P}(X_{n+1}=j\mid X_{n} = i)$  does not depend on $n$, i.e.,
$$\mathbb{P}(X_{n+1}=j\mid X_{n} = i) = \mathbb{P}(X_{1}=j \mid X_{0}=1)$$
for $n \geq 1$.

# Notation and naming conventions
Define $p_{ij}:= \mathbb{P}(X_{n+1} = j \mid X_{n} = i) = \mathbb{P}(X_{1}=j \mid X_{0}=i)$.

Note that
$$\sum_{j \in \mathscr{T}} p_{ij} = \sum_{j \in \mathscr{T}}\mathbb{P}(X_{1}=j \mid X_{0}=i)= \mathbb{P}\left( \bigcup_{j \in \mathscr{T}}\left\{  X_{1}=j  \right\}  {\bigg |} X_{0}=i\right)=1.$$
Define $P := ((p_{ij}))_{\mathscr{T} \times \mathscr{T}}$ and call it the *transition probability matrix*.

Note that 
$$P \cdot\mathbf{1}^T= \mathbf{1}^T,$$
i.e., $\mathbf{1}^T$ is an eigenvector corresponding to the eigenvalue $1$.

The distribution of $X_{0}$ is called the **initial distribution**.

# A sequence of rv is a markov chain when?
Let $\{ X_{n} \mid n \geq 0 \}$ be a sequence of random variables that takes values in $\mathscr{T}$ and $X_{0} \sim \mu$. Let $\{ \xi_{n} \mid n \geq 1 \}$ be a sequence of iid random variables, all of them being independent of $X_{0}$, that takes values in $\mathcal{T}$ and suppose that for some function $f: \mathscr{ T} \times \mathcal{T} \rightarrow \mathscr{T}$, we have $X_{n+1} = f(X_{n}, \xi_{n+1})$ for all $n \geq 0$. Then $\{ X_{n} | n\geq 0 \}$ is a homogenous markov chain.

**Note:** because of independence of $\xi_{n}'$s from $X_{0}$, we have
$$\mathbb{P}(X_{1}=j \mid X_{0}=i) = \mathbb{P}(f(X_{0}, \xi_{n+1})=j \mid X_{0} = i) = \mathbb{P}(f(i, \xi_{n+1})=j \mid X_{0}=i) = \mathbb{P}(f(i, \xi_{n+1})=j).$$


**Proof:**

$$\begin{align}
\mathbb{P}(X_{0}=i_{0};X_{1}=i_{1};\dots;X_{k} = i_{k}) &= \mathbb{P}(X_{0}=i_{0}; f(X_{0}, \xi_{1})=i_{1};\dots ;f(X_{k-1}, \xi_{k})= i_{k}) \\
&= \mathbb{P}(X_{0}=i_{0}; f(i_{0}, \xi_{1})=i_{1};\dots; f(i_{k-1}, \xi_{k})= i_{k}) \\
&= \mathbb{P}(X_{0}=i_{0})\cdot\mathbb{P}(f(i_{0}, \xi_{1})= i_{1}) \cdots \mathbb{P}(f(i_{k-1}, \xi_{k}) = i_{k}) \\
&= \mathbb{P}(X_{0}=i_{0})\prod_{j=1}^k \mathbb{P}(f(i_{j-1}, \xi_{j})=i_{j})
\end{align}$$
where the second last equality is true because $X_{0}, \xi_{1},\dots,\xi_{n}$ are independent. 


Using the above fact, (and with a slight abuse of notation) we get that
$$
\begin{align}
\mathbb{P}(X_{n+1}=j \mid X_{n}=i ; X_{n-1}= i_{n-1};\dots; X_{0}=i_{0}) &= \frac{\mathbb{P}(X_{0}=i_{0}) \prod_{j=1}^{n+1} \mathbb{P}(f(i_{j-1}, \xi_{j})=i_{j})}{\mathbb{P}(X_{0}=i_{0})\prod_{j=1}^n \mathbb{P}(f(i_{j-1}, \xi_{j})=i_{j})} \\
&= \mathbb{P}(f(i, \xi_{n+1})=j).
\end{align}
$$
Note that
$$\begin{align}
\mathbb{P}(X_{n+1}= j \mid X_{n} = i) &= \frac{\mathbb{P}(X_{n+1} = j ;X_{n}=i)}{\mathbb{P}(X_{n}=i)} \\
&= \frac{\sum_{i_{0},\dots,i_{n-1} \in \mathscr{T}}\mathbb{P}(X_{n+1}=j; X_{n}=i;X_{n-1}= i_{n-1};\dots; X_{0}=i_{0})}{\sum_{i_{0},\dots,i_{n-1} \in \mathscr{T}} \mathbb{P}(X_{n}=i;X_{n-1}= i_{n-1};\dots; X_{0}=i_{0})} \\
&= \frac{\sum_{i_{0},\dots,i_{n-1} \in \mathscr{T}}\left[ \mathbb{P}(X_{0}=i_{0}) \left(\prod_{j=1}^n \mathbb{P}(f(i_{j-1},\xi_{j}))\right) \mathbb{P}(f(i, \xi_{n+1})=j)\right]}{\sum_{i_{0},\dots,i_{n-1} \in \mathscr{T}}\left[ \mathbb{P}\left( X_{0}=i_{0}\prod_{j=1}^n \mathbb{P}(f(i_{j-1},\xi_{j})) \right) \right]} \\
&= \frac{\mathbb{P}(f(i, \xi_{n+1})=j)\cancel{\sum_{i_{0},\dots,i_{n-1} \in \mathscr{T}}\left[ \mathbb{P}(X_{0}=i_{0}) \left(\prod_{j=1}^n \mathbb{P}(f(i_{j-1},\xi_{j}))\right) \right]}}{\cancel{\sum_{i_{0},\dots,i_{n-1} \in \mathscr{T}}\left[ \mathbb{P}( X_{0}=i_{0})\prod_{j=1}^n \mathbb{P}(f(i_{j-1},\xi_{j})) \right]}} \\
&= \mathbb{P}(f(i, \xi_{n+1} )=j).
\end{align}$$
Thus, 
$$
\begin{align}
\mathbb{P}(f(i, \xi_{n+1} )=j) &= \mathbb{P}(X_{n+1}= j \mid X_{n} = i) \\
&= \mathbb{P}(X_{n+1}=j \mid X_{n}=i ; X_{n-1} = i_{n-1};\dots; X_{0}=i_{0}) \\
&= \mathbb{P}(f(i, \xi_{1})= j) \\
&= \mathbb{P}(X_{1}=j \mid X_{0}=i). 
\end{align}
$$
This proves that $\{ X_{n} | n\geq 0 \}$ is a homogeneous markov chain.

# A sequence of iid rv is a markov chain
Suppose $\{ X_{n} \mid n\geq 0 \}$ is a sequence of iid random variables that takes values in $\mathscr{T}$. Then the sequence is a markov chain.

**Proof:**
$$\begin{align}
\mathbb{P}(X_{n+1}=j \mid X_{n}=i ; X_{n-1}= i_{n-1};\dots; X_{0}=i_{0}) &= \mathbb{P}(X_{n+1}=j) \\
&= \mathbb{P}(X_{n+1}=j \mid X_{n} = i)
\end{align}$$
and we are done.

Note that, here, $p_{ij} = \mathbb{P}(X_{n+1}=j)$.

