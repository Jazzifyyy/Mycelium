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
\implies \hat{p} = \frac{n}{n + \sum_{i=1}^nx_{i}} &= \frac{1}{1+\bar{x}}.
\end{align}
$$
Note that 
$$\sum_{i=1}^n x_{i} = (0 \times 37) + (1 \times 35) + \dots + (20 \times 1) = 377$$
and $n = 150$. Thus, $\hat{p} \approx 0.2846$.

## Part b

