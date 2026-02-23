---
tags:
  - info
  - college
  - stochastic_processes
---
# Motivation and setup
We want to study a system where every individual generates off-springs according to some distribution. 

Suppose $\xi$ follows that distribution and suppose $Z_{n}$ denotes the size *of* the $n$th generation. 

Let $\xi_{i}^{(n)}$, where $n \geq 0$ and $i \geq 1$, denote the number of offsprings born to the $i$th member of the $n$th generation. We also assume that $\{ \xi_{i}^{(n)} \mid  n \geq 0, i \geq 1 \}$ makes a set of iid integer valued rvs that follows some distribution.

The process evolves according to the recurrence formula $Z_{0}=1$ (i.e., we always start with exactly one individual at the beginning) and
$$Z_{n+1} = \sum_{i=1}^{Z_{n}}\xi_{i}^{(n)}.$$
We ask the question: Does this family go extinct with probability $1$? 

We define
$$A_{n} = \{ Z_{n}=0\}$$
and we investigate the event 
$$A:= \{ Z_{n}=0 \text{ for some }n \geq 1 \} = \bigcup_{n=1}^\infty A_{n}.$$
We also define the *time of extinction* as
$$T = \inf \{  n \geq 1 \mid Z_{n} = 0 \}.$$
# Solution

## Recursive relation of the pgfs

Suppose $G$ is the pgf of $\xi$ and $P_{Z_{n}}$ is the pgf of $Z_{n}$. By our study of [[random sum properties]], we know that
$$P_{Z_{n+1}}(s) = P_{Z_{n}}(G(s))$$
for all $n \geq 0$.

By the recurrence formula of pgf, we can also obtain, for $n\geq 0$,
$$
\begin{align}
P_{Z_{n+1}}(s) &= P_{Z_{n}}(G(s)) \\
&= P_{Z_{n-1}}(G(G(s))) \\
&\text{ }\vdots \\
&= (P_{Z_{0}}\circ \underbrace{G \circ G \circ \dots \circ G}_{n+1 \text{ fold composition}})(s) \\
&= (\underbrace{G \circ G \circ \dots \circ G}_{n+1 \text{ fold composition}})(s)
\end{align}
$$
since $P_{Z_{0}}(s) = \sum_{k=0}^\infty \mathbb{P}(Z_{0}=k)s^k=1 \times s = s.$

Thus, for $n \geq 1$, we have
$$\begin{align}
P_{Z_{n}}(s) &= (\underbrace{G \circ G \circ \dots \circ G}_{n \text{ fold composition}})(s) \\
&= G(P_{n-1}(s)).
\end{align}$$

## Expectation of number of individuals at generation n

We have
$$\mathbb{E}[Z_{n+1}] = \mathbb{E}[Z_{n}].\mathbb{E}[\xi]= \mathbb{E}[Z_{n-1}].(\mathbb{E}[\xi])^2 = \dots = \mathbb{E}[Z_{0}](\mathbb{E}[\xi])^{n+1}.$$
But since $Z_{0}=1$, we have
$$\mathbb{E}[Z_{n+1}] = \mathbb{E}[\xi]^{n+1}.$$

## Connecting pgf with the probability of the concerned event

Observe that $A_{n} \subseteq A_{n+1}$ and by the continuity of the probability measure, we have
$$\begin{align}
\mathbb{P}(A) &= \mathbb{P}\left( \bigcup_{n=1}^\infty A_{n} \right) \\
&= \lim_{ n \to \infty } \mathbb{P}(A_{n}) \\
&= \lim_{ n \to \infty } P_{Z_{n}}(0)
\end{align}$$
since $A_{n} = \{ Z_{n}=0 \} \implies \mathbb{P}(A_{n}) = \mathbb{P}(Z_{n}=0) = P_{Z_{n}}(0).$

Note that we have
$$P_{Z_{n}}(0) = G(P_{Z_{n-1}}(0)).$$
Let $n \rightarrow \infty$ to get
$$\mathbb{P}(A)=G(\mathbb{P}(A)).$$
We conclude that $\mathbb{P}(A)$ is a fixed point of $G$.

(Note: One can solve to get $\mathbb{P}(A)$ from the equation if the offspring distribution is known. (See: [[exercise set 2 problem 5 stochastic processes]]))

## $\mathbb{P}(A)$ is the smallest fixed point of $G$ in $[0,1]$. 



Assume that $\mathbb{P}(\xi =1) \neq 1$. 

(The other case of $\mathbb{P}(\xi =1)=1$ is boring, because then we would have $Z_{n}=1$ for all $n\geq 1$.)

Note that $G$ is a non-decreasing function on $[0,1]$. 

Let $\tau$ be any fixed point of $G$ in $[0,1]$, i.e., $G(\tau)=\tau$ . Then
$$\begin{align}
\tau \geq 0 &\implies G(\tau) \geq G(0) \\
&\implies \tau \geq G(0) \\
&\implies G(\tau) \geq G(G(0)) \\
&\vdots \\
&\implies \tau \geq (\underbrace{G \circ G \circ \dots \circ G}_{n \text{ fold composition}})(0)=P_{Z_{n}}(0).
\end{align}$$
Let $n \rightarrow \infty$ to get
$$\tau \geq \mathbb{P}(A).$$
#### Corollary

(Recall: [[the expectation of a random variables is less than or equal to 1 iff its generating function has exactly one fixed point]])

If $G'(1)=\mathbb{E}[\xi]\leq 1$, then $G$ has only one fixed point, then $\mathbb{P}(A)=1$.

If $G'(1)=\mathbb{E}[\xi]>1$, then $G$ has two fixed points, then $\mathbb{P}(A)<1$.