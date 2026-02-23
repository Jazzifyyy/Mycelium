---
tags:
  - info
  - college
  - stochastic_processes
---
# Setup
Toss a fair coin. If $H$ turns up, move one step to the right, otherwise move one step to the left (on $\mathbb{Z}$).

Denote the $i$th random step by the random variable
$$\epsilon_{i} = \begin{cases}
+1; \text{ with probability } \frac{1}{2} \\
-1; \text{ with probability } \frac{1}{2}.
\end{cases}$$
The position of the walker at time $n$ is denoted by the random variable
$$S_{n} =\begin{cases}
a; \text{ if }n =0 \\
a+ \sum_{i=1}^n \epsilon_{i}; \text{ if }n \geq 1
\end{cases}$$
where $a \in \mathbb{Z}$.

We want to investigate that for a *simple, symmetric random walk* that starts at the origin, does the walker come back to the origin with certainty?

We define 
$$A_{n}:= \{ S_{n}=0 \}$$

and we investigate the event
$$A = \{ S_{n} =0 \text{ for some }n \geq 1 \}= \bigcup_{n=1}^\infty A_{n}.$$
Note that $A_{n} = \emptyset$ if $n$ is odd. 
# Solution
## Disjointification

We disjointify the sequence $\{ A_{n} \}$ by defining $B_{1}=A_{1}$ and
$$B_{n} = A_{n} \setminus \left( \bigcup_{k=1}^{n-1}A_{k} \right)$$
for $n \geq 1$.

Note that 
$$\bigcup_{k=1}^n A_{k} = \bigcup_{k=1}^n B_{k}; \text{ for all }n\geq 1$$
and
$$\bigcup_{k=1}^\infty A_{k} = \bigcup_{k=1}^\infty B_{k}.$$
and $\{ B_{n} \}$ is a sequence of disjoint events.

Observe that $B_{n}$ denotes the set of all walks that hits $0$ for the first time at $n$, i.e., 
$$B_{n} = \{ S_{n}=0; S_{k} \neq 0 \text{ for }k = 1,\dots,n-1\}.$$
Also note that $B_{n} = \emptyset$ if $n$ is odd. 

Define the sequence $\{ u_{n} \}$ by $u_{0}=1$ and $u_{n}:= \mathbb{P}(A_{n})$ and define the sequence $\{ f_{n} \}$ by $f_{0}=0$ and $f_{n}:= \mathbb{P}(B_{n})$.

Note that the probability that the walker comes back to zero is given by
$$\begin{align}
\mathbb{P}(A) &= \mathbb{P}\left( \bigcup_{n=1}^\infty A_{n} \right) \\
&= \mathbb{P}\left( \bigcup_{n=1}^\infty B_{n} \right) \\
&= \sum_{n=1}^\infty \mathbb{P}(B_{n}) \\
&= \sum_{n=1}^\infty f_{n} = \sum_{n=1}^\infty f_{2n}.
\end{align}$$
## Recursive relation between $\{ u_{n} \}$ and $\{ f_{n} \}$

**Claim:** We have
$$f_{2n} = u_{2n-2} - u_{2n}$$
where $n\geq 1$.

## Definitions concerning 'paths' in a random walk

**Definition:** Suppose $m<n$. A *path starting from $(m,a)$ and ending at $(n,b)$* is a finite sequence $\{ S_{m}, S_{m+1}, \dots, S_{n} \}$ such that $S_{m}=a$, $S_{n}=b$ and $|S_{k} - S_{k-1}|=1$ for $k \in \{ m+1,\dots,n \}$.  

**Definition:** Define $p$ to be the total number of $+1$ steps and $q$ to be the total number of $-1$ steps in a path.

**Definition:** Define $N_{(n,b)}^{(m,a)}$ to be the set of all paths starting at $(m,a)$ and ending at $(n,b)$. If $m=a=0$, we drop the superscript. 

The number of paths starting at $(0,0)$ and ending at $(n,a)$ is given $|N_{(n,a)}|$. 

## Deriving the number of paths

Note that if $n+a$ is odd, then either $n$ is odd and $a$ is even, or $n$ is even and $a$ is odd - which are not possible! (Think of taking a step in any direction as "flipping" the parity of $\sum \epsilon_{i}$. If $n$ is odd, then the sum must be odd, then $a$ cannot be even. Similarly, if $n$ is even, then the sum must be even, then $a$ cannot be odd.)

Also note that, by definition, we have $p+q=n$ and $p-q=a$. Solving them yields $p = \frac{n+a}{2}$ and $q = \frac{n-a}{2}$. If $n+a$ is even, then the number of paths is given by the number of ways one can put $p$ balls marked with "$+1$" in a total of $n$ boxes. 

Thus, 
$$|N_{(n,a)}| = \begin{cases}
0; \text{ if }n+a \text{ is odd} \\
{n\choose \frac{n+a}{2}}; \text{ if }n+a \text{ is even}.
\end{cases}$$

**Note:**
$$N_{(n,b)}^{(m,a)}= N_{(n-m, b-a)}.$$

## Calculating $\mathbb{P}(A_{n})$

The probability that $(\epsilon_{1},\dots,\epsilon_{n})$ takes a specified value is $\frac{1}{2^n}$ and thus, 
$$u_{2n}= \frac{1}{2^{2n}}\left|N_{(2n,0)}\right| = \frac{1}{2^{2n}} {2n \choose n}.$$
## Approximations and limits of $\{ u_{n} \}$

**Recall:** Stirling's approximation states that
$$n! \sim \sqrt{ 2\pi n }n^n e^{-n}.$$
(We say $a_{n} \sim b_{n}$ iff $\frac{a_{n}}{b_{n}} \rightarrow 1$ as $n \rightarrow \infty$.)

This implies that
$$\begin{align}
u_{2n}\sqrt{ \pi n } &= \frac{1}{2^{2n}} \frac{(2n)!}{n!n!}\sqrt{ \pi n } \\
&= \frac{(2n)!}{\sqrt{ 2\pi n }n^{2n}e^{-2n}}\cdot \frac{(\sqrt{ 2\pi n }n^n e^{-n})^2}{n!n!}\cdot \frac{1}{\sqrt{ 2 }}\cdot \frac{1}{2^{2n}} \\
&= \left(\frac{(2n)!}{\sqrt{ 2\pi 2n }(2n)^{2n}e^{-2n}}\right) \cdot \left(\frac{\sqrt{ 2\pi n }n^n e^{n}}{n!}\right)^2 \\
&\rightarrow 1
\end{align}$$
as $n \rightarrow \infty$.

Thus, 
$$u_{2n} \sim \frac{1}{\sqrt{ \pi n }}.$$
We also have
+ $u_{2n} \rightarrow 0$ as $n \rightarrow \infty$.
+ $\sum_{n=0}^\infty u_{2n} = \infty$.
## Probability of returning for some $n\geq 1$

The walker returns with certainty.
$$\begin{align}
\mathbb{P}(A) &= \sum_{n=1}^\infty f_{2n} \\
&= \sum_{n=1}^\infty (u_{2n-2}-u_{2n}) \\
&= \lim_{ N \to \infty }\sum_{n=1}^N(u_{2n-2}-u_{2n}) \\
&= \lim_{ N \to \infty } (u_{0}-u_{2}+u_{2}-u_{4}+\dots-u_{2N-2}+u_{2N-2}-u_{2N}) \\
&= \lim_{ N \to \infty }(u_{0}-u_{2N}) \\
&= u_{0}-\lim_{ N \to \infty }u_{2N}\\
&= 1. 
\end{align}$$
## Time of return

Define 
$$T:= \text{time of first return} = \inf \{ n\geq1 \mid S_{n}=0 \}.$$
Note that
$$\mathbb{P}(T=n) = \mathbb{P}(S_{n}=0; S_{k} \neq 0 \text{ for }k=1,\dots,n-1)=f_{n}.$$
What is the probability that the time of return is more than $n$?
$$\begin{align}
\mathbb{P}(T>n) &= \mathbb{P}\left( \bigcup_{k=n+1}^\infty B_{k} \right) \\
&= \sum_{k=n+1}^\infty \mathbb{P}(B_{k}) \\
&= \sum_{k=n+1}^\infty f_{k}. \\
\end{align}$$
Note that for any even number $2a$,
$$
\begin{align}
\sum_{k=2a}^\infty f_{k} &= \lim_{ N \to \infty } (f_{2a}+f_{2a+2}+\dots + f_{2a+N} \\
&= \lim_{ N \to \infty }\sum_{k=a}^{a+N}f_{2k} \\
&= \lim_{ N \to \infty } \sum_{k=a}^{a+N}(u_{2k-2}-u_{2k}) \\
&= u_{2a-2} - \lim_{ N \to \infty } u_{2a+2N} \\
&= u_{2a-2}.
\end{align}
$$


By the tail sum formula, we have
$$
\begin{align}
\mathbb{E}[T] &= \sum_{n=0}^\infty \mathbb{P}(T>n) \\
&= \sum_{n=0}^\infty \sum_{k=n+1}^\infty f_{k} \\
&= 2(f_{2}+f_{4}+\dots) + 2(f_{4}+f_{6}+\dots)+\dots \\
&= 2u_{0}+2u_{2}+\dots \\
&= 2 \sum_{n=0}^\infty u_{2n} =\infty.
\end{align}
$$
# Also See:
+ [[gambler's ruin]]