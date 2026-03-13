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
\frac{\partial l}{\partial \sigma^2} = -\frac{n}{2\sigma^2} + \frac{1}{2(\sigma^2)^2}||\mathbf{y}-X\hat{\theta}_{\text{MLE}}||^2 = 0.
$$
Thus, 
$$
\sigma^2_{\text{MLE}} = \frac{||\mathbf{y} - X\hat{\theta}_{\text{MLE}}||^2}{n}.
$$
## Part c

The MLE and LSE of $\theta$ are the same.

The estimators of $\sigma^2$ have different expression in their denominators:
$$\sigma^2_{\text{MLE}} = \frac{||\hat{\mathbf{e}}||^2}{n} \text{ v.s. } S^2 = \frac{||\mathbf{e}||^2}{n-d}.
$$
## Part d

We have
$$\begin{align}
\mathbb{E}[\hat{\theta}_{\text{MLE}}] &= \mathbb{E}[(X^TX)^{-1}X\mathbf{y}] \\
&= \mathbb{E}[(X^TX)^{-1}X(X\theta+\epsilon)] \\
&= \mathbb{E}[\theta + (X^TX)^{-1}X\epsilon] \\
&= \theta + (X^TX)^{-1}X\mathbb{E}[\epsilon]\\
&= \theta.
\end{align}$$
and
$$\begin{align}
\text{Var}(\hat{\theta}_{\text{MLE}}) &= \text{Var}[\theta + (X^TX)^{-1}X\epsilon] \\
&= [(X^TX)^{-1}X]\text{Var}(\epsilon)[(X^TX)^{-1}X]^T \\
&= (X^TX)^{-1}X^T\sigma^2I[(X^TX)^{-1}X^T]^T\\
& =\sigma^2(X^TX)^{-1}(X^TX)[(X^TX)^T]^{-1} \\
&= \sigma^2(X^TX)^{-1}.
\end{align}$$
## Part d

We have
$$\frac{||\mathbf{e}||^2}{\sigma^2}= \frac{n\hat{\sigma}^2_{\text{MLE}}}{\sigma^2} \sim \chi^2_{n-d}.$$
Then
$$\mathbb{E}\left[\frac{n\hat{\sigma}^2_{\text{MLE}}}{\sigma^2} \right] = n -d.$$
From this, we have
$$\mathbb{E}[\hat{\sigma}^2_{\text{MLE}}] = \sigma^2 \left(\frac{n-d}{n} \right).$$
We have
$$\text{Var}\left(\frac{n\hat{\sigma}^2_{\text{MLE}}}{\sigma^2} \right) = 2(n-d).$$
From this, we have
$$\text{Var}(\hat{\sigma}^2_{\text{MLE}}) = \frac{2(n-d)\sigma^4}{n^2}.$$
