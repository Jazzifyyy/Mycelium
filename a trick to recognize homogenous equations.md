---
tags:
  - info
  - college
  - books
  - differential_equations
---
A function $F$ is called *homogeneous of degree* $n$, if $F(tx,ty) = t^n F(x,y)$.   

Now suppose the functions $M$ and $N$ in the [[first-order differential equation]] are both homogeneous of the *same* degree $n$. Then we have
$$M\left( \frac{1}{x}\cdot x, \frac{1}{x}\cdot y \right) = \left( \frac{1}{x} \right)^n M(x,y)$$
i.e.,
$$M\left( 1, \frac{y}{x} \right) = \left( \frac{1}{x} \right)^n M(x,y);$$
and from this we obtain
$$M(x,y) = \left( \frac{1}{x} \right)^{-n}M\left( 1, \frac{y}{x} \right)$$
and similarly
$$N(x,y) = \left( \frac{1}{x} \right)^{-n} N\left( 1, \frac{y}{x} \right).$$
Thus, the differential equation is
$$\begin{align}
\frac{dy}{dx} &=  - \frac{M(x,y)}{N(x,y)} \\
&= - \frac{\left( \frac{1}{x} \right)^{-n}M\left( 1, \frac{y}{x} \right)}{\left( \frac{1}{x} \right)^{-n}N\left( 1, \frac{y}{x} \right)} \\
&= \frac{M\left( 1, \frac{y}{x} \right)}{N()}
\end{align}$$