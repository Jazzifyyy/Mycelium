---
tags:
  - problem
  - college
  - stochastic_processes
---
# Problem 
Find the distribution of the random variables in each of the cases and find $\mathbb{P}(X \geq n)$ for $n \geq 1$.

1. $P(s) = \frac{1}{3-2s}$
2. $P(s) = \frac{1}{4-3s}$
3. Two dice are rolled. Let $X$ be the sum of the outcomes. Find the pgf of $X$. Use this pgf to calculate the probability that the sum is divisible by $3$.
4. If the pgf of a random variable $X$ is $P(s)= \frac{1}{2}e^{s-1} + \frac{1}{4}s^2+\frac{1}{4}$, find $\mathbb{P}(X \geq 2)$.

# Solution
## Part 3

The pgf of one die is given by
$$P_{X_{1}}(s)= \frac{1}{6}(s+s^2+\dots+s^6).$$
Thus, $P_{X}(s)=(P_{X_{1}}(s))^2.$

We have
$$\mathbb{P}(X \equiv 0 (\text{mod }3))=\frac{1}{3}[P_{X}(1)+P_{X}(w)+P_{X}(w^2)]$$
where $w = e^{2\pi i/3}$.

Note that for $P(w)$ and $P(w^2)$, we have
$$s+s^2+s^3+s^4+s^5+s^6 = 2(1+w+w^2)=0$$
Thus, the required probability is 
$$\frac{1}{3}[1+0+0]=\frac{1}{3}.$$

