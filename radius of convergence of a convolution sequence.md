---
tags:
  - college
  - stochastic_processes
  - info
---
# Statement
Suppose $A(s)$ and $B(s)$ are the generating functions of $\{ a_{n} \}$ and $\{ b_{n} \}$ respectively and suppose both of them have a radius of convergence that is at least $R$.

Then the [[convolution of two sequences|convolution sequence]] $\{ c_{n} \}$ also has a radius of convergence of at least $R$.

# Proof
Since the radius of convergence of $A(s)$ is at least $R$, we have
$$R\leq \frac{1}{\limsup\limits_{n \rightarrow \infty}|a_{n}|^{1/n}} \implies \limsup\limits_{n \rightarrow \infty}|a_{n}|^{1/n} \leq \frac{1}{R}.$$
Thus, for any $\epsilon >0$, there exists $N_{1}$ such that for all $n \geq N$, we have
$$|a_{n}|^{1/n} \leq \frac{1}{R} + \epsilon \implies |a_{n}| \leq \left( \frac{1}{R} + \epsilon \right)^n.$$
Now define
$$A:= \max \left( 1, \frac{|a_{0}|}{b^0}, \frac{|a_{1}|}{b^1}, \dots , \frac{|a_{N-1}|}{b^{N-1}} \right).$$
where $b = \frac{1}{R} + \epsilon$.
Note that for all $n < N$, we have
$$\frac{|a_{n}|}{b^n}\leq A \implies |a_{n}| \leq Ab^n.$$
Also note that for all $n \geq N$, we have
$$|a_{n}| \leq b^n \leq Ab^n,$$
since $A\geq 1$.

Thus for all $\epsilon >0$, we have
$$|a_{n}| \leq A\left( \frac{1}{R} + \epsilon \right)^n$$
and
$$|b_{n}| \leq B\left( \frac{1}{R} + \epsilon \right)^n$$ for all $n$.

Now
$$\begin{align}
|c_{n}| &= \left|\sum_{k=0}^n a_{k}b_{n-k} \right| \\
&\leq \sum_{k=0}^n |a_{k}||b_{n-k}| \\
&\leq \sum_{k=0}^n A\left( \frac{1}{R}+\epsilon \right)^k B\left( \frac{1}{R} + \epsilon \right)^{n-k} \\
&= AB\left( \frac{1}{R} + \epsilon \right)^n(n+1).
\end{align}$$
This implies that for all $\epsilon>0$, we have
$$|c_{n}|^{1/n} \leq \underbrace{A^{1/n}B^{1/n}(n+1)^{1/n}}_{\text{converges to 1 as }n \rightarrow \infty}\left( \frac{1}{R} + \epsilon \right) \implies \limsup\limits_{n \rightarrow \infty}|c_{n}|^{1/n} \leq \frac{1}{R}+ \epsilon.$$
We then conclude that
$$\limsup\limits_{n \rightarrow \infty}|c_{n}|^{1/n} \leq \frac{1}{R} \implies R \leq \frac{1}{\limsup\limits_{n \rightarrow \infty}|c_{n}|^{1/n}}.$$