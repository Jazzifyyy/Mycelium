# Test of median/quantiles

Is the median say $0.2$?

We have sample $X_{1},\dots,X_{n}$.

$$H_{0}: p=\mathbb{P}(X>0.2)=\frac{1}{2}=p_{0}.$$
$$\hat{p} = \frac{1}{n}\#(X_{i}>0.2).$$
Then $n \hat{p} \sim \text{Binomial}\left( n, \frac{1}{2} \right)$ under $H_{0}$. Now perform the test. 

Either use the binomial test or normal approximation if $n$ is sufficiently large (moderately large, since binomial to normal is approximated "faster").

Is the third quartile say $0.3$?

Same setup.

$$H_{0}: p=\mathbb{P}(X>0.3)=0.25=p_{0}$$
$$H_{a}: p \neq p_{0}.$$
Once again
$$\hat{p} = \frac{1}{n}\#(X_{i} > 0.3).$$
Then $n \hat{p} \sim \text{Binomial}(n, 0.25)$ under $H_{0}$.

Then use exact binomial or normal approximation for the test (in this case, $n$ required is a little larger than for $p=\frac{1}{2}$, but still smaller than what is required for a weird distribution and hence still productive). 

Ex: given 176 observations out of 250 are less than $a=1.5$. Test if $1.5$ is the third quartile. 

$n \hat{p}=176.$
$$n \hat{p} \sim \text{Binomial}(250, 0.75).$$

$$z=\frac{176 - 250 \times 0.75}{\sqrt{ 250 \times 0.75 \times 0.25 }}=-1.68.$$
We get
$$2 \times pnorm(-1.68)= 0.0929$$
and hence do not reject $H_{0}$.

$$2 \times pbinom(176, 250, 0.75) = 0.1119$$
This is exact. 

# Estimation of cdf

$$\theta = F_{X}(t) = \mathbb{P}(X\leq t)$$
and 
$$\hat{\theta} = \frac{1}{n} \#(X_{i} \leq t).$$
$$n\hat{\theta} \sim \text{Binomial}(n, \theta).$$
So CI for $\theta$ is 
$$\hat{\theta} \pm z_{1-\frac{\alpha}{2}}\sqrt{ \frac{\hat{\theta}(1-\hat{\theta})}{n} }.$$
Note that theta hat is a function of t.

$$\hat{F}_{n}(t) = \begin{cases}
0; \text{ if }t < X_{(1)} \\
\frac{1}{n}; \text{ if } X_{(1)}\leq t < X_{(2)} \\
\vdots \\
1; t > X_{(n)}.
\end{cases}$$
The height of the steps in the graph of $\hat{F}_{n}$ is $\frac{1}{n}$ but the step lengths may vary depend on the ordered $X_{(1)}<\dots<X_{(n)}$.

Now one can get confidence intervals for all values of $t$. (Only need to compute for some $t$ values because of the stepwise nature of $\hat{F}_{n}$.)

# Testing goodness of fit of a distribution

$X_{1},\dots,X_{n} \sim F$. We want to see if $F$ is some distribution that we have in mind.
$$H_{0}: F \equiv F_{0}$$

($F_{0}$ discrete, $\chi^2$ test, $\sum \frac{(obs - exp)^2}{exp}$.)

Binning: histogram, frequency table for discrete dist. But for continuous dist, there is no obvious/objective choice of binning.

Method 1: Choose binning such that each bin has same probability under $H_{0}$ and then use chi square test.

(Code (...))

Method 2: Look at
$$D=\text{max}\{ |\hat{F}_{n}(t) - F_{0}(t)| \mid t \in \mathbb{R} \} = \text{max} \dots$$
Kolmogorov Smirnov statistic. Again, note that $t$ is maximum at one of the exteme points of a step. (No need to calculate for all $t$.)

1. Evaluation has to be done at only finitely many points.
2. $D$ is distribution free. (not obvious immediately.). Hint: $F_{X}(X) \sim \text{Uniform}$

$$\delta = \hat{F}_{n}(t) - F_{0}(t) = \#(X_{i}\leq t) \frac{1}{n} - F_{0}(t)$$
note that if the distribution is continuous, then $F_{0}$ is increasing. 

Thus, 
$$\begin{align}
\delta &= \#(F_{0}(X_{i})\leq F_{0}(t)) . \frac{1}{n} - F_{0}(t) \\
&= \#(U_{i}\leq F_{0}(t)) . \frac{1}{n} - F_{0}(t) \\
&= \#(U_{i} \leq u) . \frac{1}{n} - u \\
&= \tilde{F}_{n}(u) - u
\end{align}$$
where $U \sim Unif(0,1)$ and $\tilde{F}_{n}$ is empricial cdf of $U_{1},\dots,U_{N}$. Note that the expression is uniform which is independent of the distribution of the data.

Enough to derive the distribution of $D$ where $F_{0} \equiv U(0,1)$.

