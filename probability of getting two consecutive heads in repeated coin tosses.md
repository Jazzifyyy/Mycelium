---
tags:
  - info
  - stochastic_processes
  - college
---
Let $E_{n}$ denote the event that the experiment stops at toss $n$.

For $n \geq 3$, we have
$$\begin{align}
\mathbb{P}(E_{n}) &= \mathbb{P}(E_{n}; \epsilon_{1}=1)+ \mathbb{P}(E_{n}; \epsilon=0) \\
&= \mathbb{P}(E_{n}; \epsilon_{1}=1;\epsilon_{2}=1)+\mathbb{P}(E_{n}; \epsilon_{1}=1; \epsilon_{2}=0) + \mathbb{P}(\epsilon_{1}=0)\mathbb{P}(E_{n-1}) \\
&= \mathbb{P}(E_{n-2})\mathbb{P}(\epsilon_{1}=1)\mathbb{P}(\epsilon_{2}=0) + \mathbb{P}(\epsilon_{1}=0)\mathbb{P}(E_{n-1}) \\
&= p(1-p)p_{n-2} + (1-p)p_{n-1}.
\end{align}$$
Let $T$ denote the time of stopping and let $P$ be the associated pgf. Then
$$\begin{align}
P(s) &= \sum_{n=2}^\infty p_{n}s^n \\
&= p_{2}s^2 + \sum_{n=3}^\infty p_{n}s^n \\
&= p_{2}s^2 + \sum_{n=3}^\infty (1-p)p_{n-1}s^n + p(1-p)\sum_{n=3}^\infty p_{n-2}s^n \\
&= p_{2}s^2 + (1-p)s\sum_{n=2}^\infty p_{n}s^n + p(1-p)s^2\sum_{n=1}^\infty p_{n}s^n \\
&= p^2s^2 + (1-p)sP(s) + p(1-p)s^2 P(s).
\end{align}$$
By the above equation, we get that
$$\begin{align}
P(1) &= p^2 + (1-p)P(1) + p(1-p)P(1) \\
\implies 
\end{align}$$