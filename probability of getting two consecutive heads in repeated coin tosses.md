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
&= p(1-p)p_{n-2} + (1-p)p_{n-1}
\end{align}$$