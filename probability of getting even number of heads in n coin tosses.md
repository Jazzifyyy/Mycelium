---
tags:
  - college
  - stochastic_processes
  - problem
---
# Problem

A coin is tossed $n$ times independently. What is the probability of getting an even number of heads?

# Solution

Let $p$ denote the probability of getting heads in a coin toss.

Define
$$\epsilon_{i} = \begin{cases}
1; \text{ if coin toss i is H} \\
0; \text{ otherwise.}
\end{cases}$$
and
$$S_{n} = \sum_{i=1}^n \epsilon_{i}$$
which denotes the total number of heads in $n$ coin tosses; and $S_{0}=0$.

We want to find $p_{n}:= \mathbb{P}(S_{n} \text{ is even})$.

Note that $p_{0}=1$ and $p_{1}=\mathbb{P}(S_{n} \text{ is even})= \mathbb{P}(\epsilon_{1}=0)=1-p$.

Note that, for $n\geq 0$,
$$\begin{align}
p_{n+1} &= \mathbb{P}(S_{n+1} \text{ is even}) \\
&= \mathbb{P}(S_{n+1} \text{ is even}; \epsilon_{n+1}=1)+\mathbb{P}(S_{n+1} \text{ is odd}; \epsilon_{n+1}=0) \\
&= \mathbb{P}(S_{n} \text{ is odd}; \epsilon_{n+1}=1) + \mathbb{P}(S_{n} \text{ is even}; \epsilon_{n+1}=0) \\
&= \mathbb{P}(S_{n} \text{ is odd}).\mathbb{P}(\epsilon_{n+1}=1) + \mathbb{P}(S_{n} \text{ is even}). \mathbb{P}(\epsilon_{n+1}=0) \\
&= (1-p_{n})p+p_{n}(1-p).
\end{align}$$

Alternative approach, for $n\geq 0$:
$$\begin{align}
p_{n+1} &= \mathbb{P}(S_{n+1} \text{ is even}) \\
&= \mathbb{P}(S_{n+1} \text{ is even}; \epsilon_{1}=1) + \mathbb{P}(S_{n+1}\text{ is even}; \epsilon_{1}=0) \\
&= \mathbb{P}(S_{n+1}-S_{n} \text{ is odd}; \epsilon_{1}=1) + \mathbb{P}(S_{n+1}-S_{n} \text{ is even}; \epsilon_{1}=0) \\
&= \mathbb{P}(S_{n+1}-S_{n} \text{ is odd}).\mathbb{P}(\epsilon_{1}=1) + \mathbb{P}(S_{n+1}-S_{n} \text{ is even}).\mathbb{P}(\epsilon_{1}=0).
\end{align}$$
Note that since the coin tosses are independent, we have 
$$S_{n} \overset{d}{=} S_{n+1}-S_{1}.$$
Thus,
$$\begin{align}
p_{n+1}&= \mathbb{P}(S_{n} \text{ is odd}).\mathbb{P}(\epsilon_{1}=1) + \mathbb{P}(S_{n} \text{ is even}). \mathbb{P}(\epsilon_{1}=0) \\
&= (1-p_{n})p+p_{n}(1-p).
\end{align}$$

The generating function associated with this sequence is
$$P(s)=\sum_{n=0}^\infty p_{n}s^n.$$

Note that
$$\begin{align} 
P(s)-1 &= \sum_{n=0}^\infty p_{n+1}s^{n+1} \\
 &= \sum_{n=0}^\infty (1-p_{n})ps^{n+1} + \sum_{n=0}^\infty p_{n}(1-p)s^{n+1} \\
&= ps\sum_{n=0}^\infty s^n -ps\sum_{n=0}^\infty p_{n}s^n + (1-p)s\sum_{n=0}^\infty p_{n}s^n \\
&= \frac{ps}{1-s}  - psP(s) + (1-p)s P(s) \\
&= \frac{ps}{1-s} +sP(s)(1-2p).
\end{align}$$
This implies that
$$P(s)(1-s+2ps) = \frac{ps}{1-s}+1 = \frac{ps+1-s}{1-s}.$$
Thus,
$$P(s) = \begin{cases}
\frac{1- s/2}{1-s}; \text{ if }p = \frac{1}{2} \\
\frac{ps-s+1}{(1-s)(1-s+2ps)}; \text{ if }p \neq \frac{1}{2}. 
\end{cases}$$
Note that
$$\begin{align}
\frac{1- s/2}{1-s} &= \frac{1}{1-s} - \frac{1}{2}\cdot\frac{s}{1-s} \\
&= \sum_{n=0}^\infty s^n - \frac{1}{2}\sum_{n=0}^\infty s^{n+1} \\
&= \sum_{n=0}^\infty s^n - \frac{1}{2}\sum_{n=1}^\infty s^{n} \\
&= 1 + \sum_{n=1}^\infty s^n - \frac{1}{2}\sum_{n=1}^\infty s^n \\
&= 1+ \frac{1}{2}\sum_{n=1}^\infty s^n \\
&= 1 + \frac{1}{2}s + \frac{1}{2}s^2 + \dots \infty. \\
\end{align}$$
Compare them term by term with $\sum p_{n}s^n$ to conclude that $p_{0}=1$ and $p_{n} = \frac{1}{2}$ for all $n \geq 1$.

Now note that 
$$\begin{align}
\frac{1-(1-p)s}{(1-s)(1-s+2ps)} &= \frac{A}{1-s}+ \frac{B}{1-s+2ps}
\end{align}$$
where $A$ and $B$ satisfies
$$1-(1-p)s = A(1-s+2ps) + B(1-s).$$
Thus, we have
$$A+B=1 \text{ and } -(1-p)=A(2p-1)-B.$$
Solving them yields $A=B=\frac{1}{2}$.

Thus,
$$\begin{align}
P(s) &= \frac{1}{2}\cdot \frac{1}{1-s} + \frac{1}{2} \cdot \frac{1}{1-s(1-2p)} \\
&= \frac{1}{2}\sum_{n=0}^\infty s^n + \frac{1}{2}\sum_{n=0}^\infty (1-2p)^ns^n \\
&= \sum_{n=0}^\infty \left( \frac{1}{2} + \frac{1}{2}(1-2p)^n \right)s^n.
\end{align}$$
Compare them term by term with $\sum p_{n}s^n$ to conclude that 
$$p_{n} = \frac{1}{2} + \frac{1}{2}(1-2p)^n$$
for all $n\geq 0$.

If $0<p<1$, then $p_n \rightarrow \frac{1}{2}$ as $n \rightarrow \infty$. 