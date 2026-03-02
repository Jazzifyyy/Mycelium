---
tags:
  - info
  - statistical_methods
  - college
---
## Part a

The likelihood function is given by
$$L(p) = \prod_{i=1}^n p(1-p)^{x_{i}} = p^n(1-p)^{\sum_{i=1}^n x_{i}}.$$
The log-likelihood function is given by
$$\mathcal{L}(p) = n \log p + \left( \sum_{i=1}^n x_{i}\right)\log(1-p).$$
Differentiate with respect to $p$ and set it equal to zero to get
$$
\begin{align}
\frac{n}{\hat{p}} - \frac{\sum_{i=1}^n x_{i}}{1-\hat{p}} &= 0 \\
\implies n+\hat{p}\left( -n- \sum_{i=1}^n x_{i} \right) &= 0 \\
\implies \hat{p} &= \frac{n}{n + \sum_{i=1}^nx_{i}}
\end{align}
$$