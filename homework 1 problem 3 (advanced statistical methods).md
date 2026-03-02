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

Note that
$$\begin{align}
\mathbb{P}(A) &= \mathbb{P}(X > 3) \\
&= p(1-p)^4 \sum_{k=0}^\infty (1-p)^k \\
&= p(1-p)^4 \cdot \frac{1}{1-(1-p)} \\
&= (1-p)^4 
\end{align}$$
and thus, $\hat{\mathbb{P}}_{\text{MLE}}(A) = (1 - \hat{p})^4 \approx (1-0.2846)^4 \approx 0.2619.$

## Part c

A non-parametric estimate of $\mathbb{P}(A)$ is the empericial number of accidents where the gap was greater than $3$ days:
$$\hat{\mathbb{P}}(A) = \frac{8 + 4+7+\dots + 1}{150} = \frac{32}{150} \approx 0.2133.$$
## Part d

```r
n <- 150
sum_xi <- 377

theta_hat <- 0.2133

exact_test <- binom.test(32, 150, conf.level = 0.95)
print(exact_test)
```
The exact confidence interval for $\theta$ is
```
95 percent confidence interval:
 0.1507302 0.2876066
```