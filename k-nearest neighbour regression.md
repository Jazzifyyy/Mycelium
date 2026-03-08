---
tags:
  - info
  - college
  - statistical_methods
  - non_parametric
---
This is a technique used in the context of [[non-parametric regression]].

The estimate of the function $f$ at $x$ is given by the average of those $y_{i}'$s for which the corresponding $x_{i}'$s are not further than $k$ from $x$, i.e., 
$$\hat{f}(x) = \frac{\sum_{i=1}^n w_{i}(x)y_{i}}{\sum_{i=1}^n w_{i}(x)}$$
where 
$$w_{i}(x) = \begin{cases}
1; \text{ if }|x - x_{i}|<k; \\
0; \text{ otherwise}.
\end{cases}$$
