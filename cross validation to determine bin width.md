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
Note that the third term does not involve $h$ and the second term is $-2\mathbb{E}[\hat{f}_{h}(X)]$ where $X \sim f$.

Recall that we had $X_{1},\dots,X_{n} \overset{\text{iid}}{\sim}f$ and thus the second term can be estimated by
$$\frac{1}{n} \sum_{i=1}^n \hat{f}_{h}(X_{i})$$
but this is biased, since after denoting $K_{h}(x - X_{j}) = \frac{1}{h_{n}}K\left(\frac{x- X_{j}}{h_{n}}\right)$, we have
$$\begin{align}
\mathbb{E}\left[\frac{1}{n} \sum_{i=1}^n \hat{f}_{h}(X_{i})\right] &= \mathbb{E}[\hat{f}_{h}(X_{i})] \\
&= \mathbb{E}\left[ \frac{1}{n}\sum_{j=1}^n K_{h}(X_{i} - X_{j}) \right] \\
&= \frac{1}{n}[(n-1)\mathbb{E}[\hat{f}_{h}(X_{i})] + \mathbb{E}[K_{h}(0)]] \\
&= \mathbb{E}\left[ \hat{f}_{n}(X_{i}) \right] + \underbrace{\frac{1}{n}\left(K_{h}(0) - \mathbb{E}[\hat{f}_{h}(X_{i})]\right)}_{\text{Bias}}.
\end{align}$$
The bias can be corrected by removing the $K_{h}(X_{i}-X_{i})$ term in the sum
