---
tags:
  - info
  - college
  - statistical_methods
  - non_parametric
---
# Goal
Suppose $X_{1},\dots,X_{n}$ is a random sample from pdf $f$. We want to estimate the parameter $f$. 

(Note that $f$ is an infinite dimensional parameter.)

# Shifted Histogram

We can estimate $f$ by a histogram. In such a case, we have the desirable properties: $\int \hat{f}(x)dx=1$ and $\hat{f} \geq 0$.

For any $t$, where 
$$x=:x_{i}< t< x_{i+1}:= x + \delta,$$
the estimate at $t$ is given by

$$\hat{f}(t)= \frac{\# (X_{i} \in (x, x + \delta))}{n \delta} = \frac{\hat{F}_{n}(x + \delta) - \hat{F}_{n}(x)}{\delta}.$$
Note that 
$$\hat{f}(t) \sim \frac{1}{n\delta}\text{Binomial}(n, F(x + \delta)-F(x)).$$
Denote $p:=F(x + \delta)-F(x)$.

Thus,
$$\mathbb{E}[\hat{f}(t)] = \frac{1}{n\delta}\cdot n(F(x + \delta)-F(x)) = \frac{F(x + \delta)- F(x)}{\delta}= \frac{p}{\delta}$$
and
$$\text{Var}(\hat{f}(t)) = \frac{1}{n^2 \delta^2}\cdot np(1-p) = \frac{p(1-p)}{n \delta^2}.$$

The mean squared error is given by
$$\text{MSE} = \text{Bias}^2 + \text{Var} = \left( \frac{p}{\delta} -f (t)\right)^2 + \frac{p(1-p)}{n\delta^2}.$$
Problems: 
1. Histogram is not smooth
2. Location and width of the bins are subjective. 

First problem solution:

We may minimize this expression over $\delta$ to get the optimal banwidth.

Second problem solution:

First note that 
$$f(x) \approx \frac{F\left( x + \frac{h}{2} \right) - F\left( x - \frac{h}{2} \right)}{h}$$
for small $h > 0$. This leads to the estimator
$$
\begin{align}
\hat{f}_{n}(x) &= \frac{1}{nh_{n}}\left[ F_{n}\left( x + \frac{h_{n}}{2} \right)  - F_{n}\left( x - \frac{h_{n}}{2} \right) \right] \\
&= \frac{1}{nh_{n}}\sum_{i=1}^n \mathbb{1}\left( x - \frac{h_{n}}{2}\leq X_{i} \leq x +\frac{h_{n}}{2} \right] \\
&= \frac{1}{nh_{n}}\sum_{i=1}^n \mathbb{1}\left( -\frac{1}{2} \leq \frac{x - X_{i}}{h_{n}} \leq \frac{1}{2}\right] \\
&= \frac{1}{nh_{n}}\sum_{i=1}^n \mathbb{1}_{\left( -\frac{1}{2}, \frac{1}{2} \right]}\left(\frac{x- X_{i}}{h_{n}} \right).
\end{align}
$$
Intuition: Consider a distribution with mass $\frac{1}{n}$ at each $X_{i}$. If we "spread" that discrete mass uniformly over an interval of length $h_{n}$ centered around $X_{i}$, then the mass at $\frac{1}{n}$ is replaced by a histogram of height $\frac{1}{n h_{n}}$ on the interval $(X_{i} - h/2, X_{i} + h /2]$. Put all the histograms around $X_{1},\dots,X_{n}$ together to obtain $\hat{f}_{n}$.

But note that the mass $\frac{1}{n}$ at each $X_{i}$ can be spread by any arbitrary manner. This would define a general class of estimators of the form 
$$\hat{f}_{n}(x) = \frac{1}{nh_{n}}\sum_{i=1}^n K\left(\frac{x - X_{i}}{h_{n}} \right)$$
where $K$ is a pdf (i.e., $K(u)\geq 0$ and $\int_{-\infty}^\infty K(u)du=1$). Such an estimator is called a **Kernel estimator** with *kernel* $k$ and *bandwidth* $h_{n}$.

Note that 
$$\begin{align}
\mathbb{E}[\hat{f}_{n}(x)] &= \mathbb{E}\left[\frac{1}{nh_{n}}\sum_{i=1}^n K\left(\frac{x - X_{i}}{h_{n}} \right)\right] \\
&= \mathbb{E}\left[ \frac{1}{h_{n}}K\left(\frac{x - X_{i}}{h_{n}} \right) \right] \\
&= \int_{-\infty}^\infty \frac{1}{h_{n}}K\left(\frac{x- y}{h_{n}}\right)f(y)dy \\
\text{ Set }u&= \frac{x - y}{h_{n}} \text{ with }dy = -h_{n}du  \\
&=\int_{-\infty}^\infty -\left[ \frac{1}{h_{n}}K(u)f(x - h_{n}u) \right](-h_{n}du) \\
&= \int_{-\infty}^\infty K(u)f(x - h_{n}u)du.
\end{align}$$
Similarly, 
$$
\begin{align}
\text{Var}(\hat{f}_{n}(x)) &= \frac{1}{n^2h_{n}^2}\text{Var}\left[\sum_{i=1}^n K\left( \frac{x - X_{i}}{h_{n}} \right) \right] \\
&= \frac{1}{nh_{n}^2}\text{Var}\left[K\left(\frac{x- X_{i}}{h_{n}} \right)\right] \\
&= \frac{1}{n}\left\{ \frac{1}{h_{n}}\mathbb{E}\left[ \frac{1}{h_{n}}K^2\left( \frac{x - X_{i}}{h_{n}} \right) \right] - \mathbb{E}[\hat{f}_{n}(x)]^2\right\} \\
&= \frac{1}{n} \left\{  \frac{1}{h_{n}}\int_{-\infty}^\infty K^2(u)f(x - h_{n}u)du - \left( \int_{-\infty}^\infty K(u)f(x - h_{n}u)du \right)^2  \right\}.
\end{align}
$$
We make the following assumptions:
1. $K(u)= K(-u)$ for all $u$, $\sigma^2_{K} = \int_{-\infty}^\infty u^2K(u)du < \infty$, and $\lvert \lvert K \rvert  \rvert^2 = \int_{-\infty}^\infty K^2(u)du < \infty$.
2. $f''$ is bounded and continuous.

Note that by taylor's theorem, we can expand $f(x - h_{n}u)$ by setting $x'=x-h_{n}u$ and $a=x$ in
$$f(x') = f(a) + f'(a)(x'-a) + \frac{f''(c)}{2}(x'-a)^2$$
where $c$ lies between $x'$ and $a$, i.e.,
$$\begin{align}
f(x - h_{n}u) &= f(x) -h_{n}u f'(x) + \frac{f''(x - \lambda h_{n}u)}{2}h_{n}^2u^2 \\
&= f(x) - h_{n}uf'(x) + \frac{1}{2}h_{n}^2u^2f''(x) + \frac{1}{2}h_{n}^2u^2(f''(x - \lambda h_{n}u) - f''(x))
\end{align}$$
where $0 \leq \lambda \leq 1$.

Now note that since $h_{n}u \rightarrow 0$ as $n \rightarrow \infty$, we have $f''(x - h_{n}u) \rightarrow f''(x)$ as $n \rightarrow \infty$, since $f''$ was taken to be continuous.

Note that since $f''$ is bounded, say by $M$, we have
$$|f''(x- h_{n}u) - f''(x)| \leq 2M$$
and thus
$$|(f''(x-h_{n}u) - f''(x))u^2K(u)|\leq 2Mu^2K(u).$$
Note that the rhs is integrable by one of the assumptions, and thus by dominated convergence theorem, we have
$$\lim_{ n \to \infty } \int_{-\infty}^\infty (f''(x - h_{n}u) - f''(x))u^2K(u)du= 0.$$
All of this allows us to the bias and variance of the kernel estimator:
$$\begin{align}
\mathbb{E}[\hat{f}_{n}(t)] &= \int_{-\infty}^\infty K(u)f(x - h_{n}u)du \\
&= \int_{-\infty}^\infty \left[ K(u)f(x) - h_{n}f'(x)uK(u) + \frac{1}{2}h_{n}^2 f''(x)u^2K(u) \right]du  \\
&+ \frac{1}{2}h_{n}^2\int_{-\infty}^\infty (f''(x - h_{n}u) - f''(x))u^2K(u)du \\
&= f(x) + \frac{1}{2}h_{n}^2f''(x)\sigma^2_{K} + \frac{1}{2}h_{n}^2o(1).
\end{align}$$
It then follows that
$$\text{Bias}[\hat{f}_{n}(t)] = \frac{1}{2}h_{n}^2[f''(x)\sigma^2_{K} +o(1)].$$
Also,
$$\begin{align}
\int_{-\infty}^\infty K^2(u)f(x - h_{n}u)du &= \int_{-\infty}^\infty \left[ K^2(u)f(x) - h_{n}f'(x)uK^2(u) + \frac{1}{2}h_{n}^2f''(x)u^2K^2(u)\right]du +(\dots)\\
&= f(x) \lvert \lvert K \rvert  \rvert^2  +  o(1) \\

\end{align}
$$

$$\text{Var}(\hat{f}_{n}(t)) = \frac{1}{nh_{n}}[\lvert \lvert K \rvert  \rvert ^2f(x) + o(1)].$$
Combining them, we have
$$
\begin{align}
\text{MSE}[\hat{f}_{n}(t)] &= h_{n}^4\left[ \frac{\sigma^4_{K}f''(x)^2}{4}  + o(1)\right] + \frac{1}{nh_{n}}[\lvert \lvert K \rvert  \rvert^2f(x)+o(1) ] \\
\implies n^{4/5}\text{MSE}[\hat{f}_{n}(t)] &= (n^{1/5}h_{n})^4\left[ \frac{\sigma^4_{K}f''(x)^2}{4} + o(1)\right] + (n^{1/5}h_{n})^{-1}[\lvert \lvert K \rvert  \rvert^2f(x)+o(1) ]. 
\end{align}
$$
Note that on the rhs of the equation, the first term $\rightarrow \infty$ if $n^{1/5}h_{n} \rightarrow \infty$ and the second term $\rightarrow \infty$ if $n^{1/5}h_{n} \rightarrow 0$. 

Thus to ensure that the MSE does not blow up, $h_{n}$ must be of order of magnitude, i.e., $h_{n} = tn^{-1/5}$. Then,

$$
\begin{align}
\text{MSE}[\hat{f}_{n}(t)] &= t^4\left[ \frac{\sigma^4_{K}f''(x)^2}{4} + o(1)\right] + t^{-1}[\lvert \lvert K \rvert  \rvert^2f(x)+o(1) ] \\
&= \frac{t^4\sigma^4_{K}f''(x)^2}{4} + \frac{1}{t} \lvert \lvert K \rvert  \rvert^2f(x) + o(1). 
\end{align}
$$
Now note that $t^4a + t^{-1}b$ where $a,b>0$ is maximized if
$$4t^3a -\frac{1}{t^2}b=0 \implies 4t^5a=b \implies t = \frac{b}{}$$