---
tags:
  - linear_statistical_models
  - info
  - college
---
# Model
$$y_{i} = \alpha + \beta_{1}x_{1i}+ \dots + \beta_{p}x_{pi} + \epsilon_{i}.$$
We observe $(x_{11}, x_{21}, \dots, x_{p1}, y_{1}), \dots, (x_{1n}, x_{2n}, \dots, x_{pn}, y_{n})$.

Assumptions:
+ $\mathbb{E}[\epsilon_{i}] = 0$ for all $i \in \{ 1,\dots,n \}$, i.e., on average we make no error.
+ $\text{Var}(\epsilon_{i}) = \sigma^2$ for all $i \in \{ 1,\dots,n \}$, i.e., errors are of the same scale, also known as *homoscedastic errors*.
+ $\text{Cov}(\epsilon_{i}, \epsilon_{j}) = 0$ for all $i \neq j$, i.e., the errors made on two different observations are uncorrelated.
# Representation in terms of linear algebra
Our model can be rewritten as
$$
\begin{align}
\mathbf{y} &= \alpha \mathbf{1} + \beta_{1}\mathbf{x}^{(1)}+ \dots + \beta_{p}\mathbf{x}^{(p)} + \tilde{\epsilon} \\
&= \begin{pmatrix}
\mathbf{1} & \mathbf{x}^{(1)} & \dots & \mathbf{x}^{(p)}
\end{pmatrix}
\begin{pmatrix}
\alpha \\
\beta_{1} \\
\vdots \\
\beta_{p}
\end{pmatrix} + \tilde{\epsilon} \\
&= X \tilde{\theta} + \tilde{\epsilon}.
\end{align}$$
where $\mathbf{y} = (y_{1}, \dots, y_{n})^T, \mathbf{1} = (1,\dots,1)^T, \mathbf{x}^{(1)} = (x_{11},x_{12}, \dots, x_{1n})^T,\dots,\mathbf{x}^{(p)} = (x_{1p},x_{p2}, \dots, x_{pn})^T,\tilde{\epsilon} = (\epsilon_{1},\dots,\epsilon_{n})^T$and 
$$
\begin{align}
X_{n \times (p+1)} &= \begin{pmatrix}
\mathbf{1} & \mathbf{x}^{(1)} & \dots & \mathbf{x}^{(p)}
\end{pmatrix} \\
&= \begin{pmatrix}
1 & x_{11} & \dots & x_{p1} \\
1 & x_{12} & \dots & x_{p2} \\
\vdots & \vdots & \ddots & \vdots \\
1 & x_{1n} & \dots & x_{pn}
\end{pmatrix}
\end{align}
$$
is the **data matrix** and
$$\tilde{\theta} = (\alpha, \beta_{1},\dots,\beta_{p})^T$$ is the **parameter vector**.

Assumptions:
+ $\mathbb{E}[\tilde{\epsilon}] = \mathbf{0}$.
+ $\text{Var}(\tilde{\epsilon}) = \sigma^2I$.

# Short hand representation of a regression model

The model above can be summarized by writing $(\mathbf{y}, X\tilde{\theta}, \sigma^2I)$. This is also known as the **Gauss-Markov setup** which would be the focus for now.

More generally, we have $(\mathbf{y}, X\tilde{\theta}, \Sigma)$.

# Also See:
+ [[parameter estimation of a regression model]]