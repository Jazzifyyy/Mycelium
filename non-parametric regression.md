---
tags:
  - info
  - college
  - statistical_methods
  - non_parametric
---
General regression:
$$y = f(x)+ \epsilon$$

In non-parametric regression, we do not assume any functional form of the dependence between $x$ and $y$, i.e., we make no assumption on $f$, apart from the assumption that it is "smooth" (i.e., it is continuos and derivatives exists till a certail degree or they turn zero after a certain degree).

Suppose $(X,Y)$ are random, and we want to minimize $\mathbb{E}[(Y - \hat{f}(X))^2]$. Note:
$$\begin{align}
\mathbb{E}[(Y - \hat{f}(X))^2] &= \mathbb{E}[(Y - \mathbb{E}[Y|X] + \mathbb{E}[Y|X] - \hat{f}(X))^2] \\
&= \mathbb{E}[(Y - \mathbb{E}[Y|X])^2] + \mathbb{E}[(\mathbb{E}[Y|X] - \hat{f}(X))^2] + \mathbb{E}[(Y - \mathbb{E}[Y|X])(\mathbb{E}[Y|X] - \hat{f}(X))] \\
&= \mathbb{E}[(Y - \mathbb{E}[Y|X])^2] + \mathbb{E}[(\mathbb{E}[Y|X] - \hat{f}(X))^2].
\end{align}$$
