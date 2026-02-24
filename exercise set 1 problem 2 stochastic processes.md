---
tags:
  - problem
  - stochastic_processes
  - college
---
# Problem 
Find the pgf of the following random variables and state their radius of convergence:
1. $X$ where $\mathbb{P}(X=n) = \frac{c}{n!}$ for $n\geq 0$. Find the constant $c$ first.
2. $Y$ where $\mathbb{P}(Y=n) = \frac{c}{(n+1)(n+2)}$ for $n \geq 0$. Find the constant $c$ first.
3. $Z$ where $\mathbb{P}(Z=n) = \frac{1}{2^{n+1}}$ for $n \geq 0$.

# Solution
## Part 1
We must have
$$\begin{align}
1 &= \sum_{n=0}^\infty \frac{c}{n!} \\
&= c\cdot e
\end{align}$$
and thus $c = \frac{1}{e}$.

The pgf is given by
$$
\begin{align}
G_{X}(s) &= \sum_{n=0}^\infty \left( \frac{e^{-1}}{n!} \right)s^n \\
&= e^{-1}\sum_{n=0}^\infty \frac{s^n}{n!} \\
&= e^{s-1}.
\end{align}
$$
This is well-defined for all $s$. Thus, $R = \infty$.

## Part 2

We must have
$$\begin{align}
1 &= \sum_{n=0}^\infty \frac{c}{(n+1)(n+2)} \\
&= c\sum_{n=0}^\infty\left[ \frac{1}{n+1} - \frac{1}{n+2} \right] \\
&= c \left[  1 - \frac{1}{2} + \frac{1}{2} - \frac{1}{3} + \dots \right] \\
&= c.
\end{align}$$
The pgf is given by
$$\begin{align}
G_{Y}(s) &= \sum_{n=0}^\infty \frac{s^n}{(n+1)(n+2)}.
\end{align}$$

The pgf converges if 
$$\lim_{ n \to \infty } \left|\frac{s^{n+1}(n+1)(n+2)}{(n+2)(n+3)s^n}\right| = |s|\lim_{ n \to \infty } \left| \frac{n+1}{n+3} \right| = |s|<1.$$
