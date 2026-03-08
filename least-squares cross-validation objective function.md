---
tags:
  - info
  - college
  - statistical_methods
---
We aim to minimize 
$$
\begin{align}
\int_{-\infty}^\infty (\hat{f}_{h}(x) -f(x))^2dx &=\int_{-\infty}^\infty \hat{f}^2_{h}(x)dx  - 2 \int_{-\infty}^\infty \hat{f}_{h}(x)f(x)dx + \int_{-\infty}^\infty f^2(x)dx.
\end{align}
$$
Note that the third term does not involve $h$, and the first term can be computed since we can compute $\hat{f}_{h}(x)$ for every $x$, and the second term is $-2\mathbb{E}[\hat{f}_{h}(X)]$ where $X \sim f$.

Recall that we had $X_{1},\dots,X_{n} \overset{\text{iid}}{\sim}f$ and thus the second term can be estimated by
$$(-2)\frac{1}{n} \sum_{i=1}^n \hat{f}_{h}(X_{i})$$
but this is biased, since after denoting $K_{h}(x - X_{j}) = \frac{1}{h_{n}}K\left(\frac{x- X_{j}}{h_{n}}\right)$, we have
$$\begin{align}
\mathbb{E}\left[\frac{1}{n} \sum_{i=1}^n \hat{f}_{h}(X_{i})\right] &= \mathbb{E}[\hat{f}_{h}(X_{i})] \\
&= \mathbb{E}\left[ \frac{1}{n}\sum_{j=1}^n K_{h}(X_{i} - X_{j}) \right] \\
&= \frac{1}{n}[(n-1)\mathbb{E}[\hat{f}_{h}(X_{i})] + \mathbb{E}[K_{h}(0)]] \\
&= \mathbb{E}\left[ \hat{f}_{n}(X_{i}) \right] + \underbrace{\frac{1}{n}\left(K_{h}(0) - \mathbb{E}[\hat{f}_{h}(X_{i})]\right)}_{\text{Bias}}.
\end{align}$$
The bias can be corrected by ensuring that the $K_{h}(X_{i}-X_{i})$ term does not appear in the density estimate, i.e., 
$$\hat{f}_{h, -i}(X_{i}) = \frac{1}{n-1}\sum_{j \in \{ 1,\dots,n  \} \setminus \{ i \}}K_{h}(X_{i}-X_{j}).$$
Thus, $(-2) \frac{1}{n}\sum_{i=1}^n \hat{f}_{h, -i}(X_{i})$ estimates the second term.

Thus, the final objective is to pick an $h$ that minimizes the **least-squares cross-validation objective function**:
$$\text{LSCV}(h) =\int_{-\infty}^\infty \hat{f}_{h}(x)^2 dx - \frac{2}{n}\sum_{i=1}^n \hat{f}_{h, -i}(X_{i}).$$

