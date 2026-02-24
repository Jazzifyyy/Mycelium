---
tags:
  - books
  - stochastic_processes
  - info
---
(See: [[probability generating function]])
# Statement
Suppose $X,Y$ are two independent non-negative integer valued random variables. Then 
$$P_{X+Y}(s) = P_{X}(s)P_{Y}(s).$$
# Proof
We have
$$\begin{align}
P_{X+Y}(s) &= \mathbb{E}[s^{X+Y}] \\
&= \mathbb{E}[s^Xs^Y] \\
&= \mathbb{E}[s^X]\mathbb{E}[s^Y] \\
&= P_{X}(s)P_{Y}(s).
\end{align}$$
