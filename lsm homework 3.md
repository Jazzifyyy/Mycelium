# Problem 1
## Part a

The likelihood function is given by
$$
L(\mathbf{\theta}, \sigma^2) = \frac{1}{(2\pi \sigma^2)^{n/2}}\exp \left\{  -\frac{1}{2\sigma^2}(\mathbf{y} - X\mathbf{\theta})^T(\mathbf{y} - X\theta)  \right\}.
$$
The log-likelihood function is given by
$$l(\theta, \sigma^2) = - \frac{n}{2} \ln(2\pi) - \frac{n}{2}\ln(\sigma^2) - \frac{1}{2\sigma^2} ||\mathbf{y}-X\theta||^2.$$
## Part b

We must have that $\hat{\theta}_{\text{MLE}}$ maximizes $l$, i.e., it minimizes $||\mathbf{y} - X\theta||^2$. Thus,
$$
\hat{\theta}_{\text{MLE}} = (X^TX)^{-1}X^T\mathbf{y}.
$$
We must also have
$$
\frac{\partial l}{}
$$