---
tags:
  - info
  - college
  - books
  - differential_equations
---
# The trick

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
&= -\frac{M\left( 1, \frac{y}{x} \right)}{N\left( 1, \frac{y}{x} \right)}.
\end{align}$$
The rhs is a function of the form $g\left( \frac{y}{x} \right)$, and therefore is a [[first order homogeneous equation]].
# Example
## Example 1

Consider 
$$(y + \sqrt{ x^2 + y^2 })dx - xdy=0$$
Note that $N$ is of degree $1$ and
$$M(tx,ty) = ty + \sqrt{ (tx)^2 + (ty)^2 } = t(y + \sqrt{ x^2 + y^2 }) = tM(x,y)$$
is also of degree $1$, and thus the equation is a homogeneous equation.