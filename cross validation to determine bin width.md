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
$$\frac{1}{n} \sum_{i=1}^n \hat{f}_{h}(X_{i}).$$
