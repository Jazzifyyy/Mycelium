---
tags:
  - problem
  - college
  - differential_equations
---
# Problem 
Obtain the differential equations of the family of ellipses with foci at $(-1,0)$ and $(1,0)$.

# Solution
Fact: Sum of the focal distances of a point on the ellipse is a constant and is equal to the length of its major axis.

Thus for any point $(x,y)$ on the ellipse, we have

$$\sqrt{ (x+1)^2 +y^2 } + \sqrt{ (x-1)^2 + y^2 }=2a$$
where $a>1$.

Then
$$\begin{align}
\sqrt{ (x+1)^2 + y^2 } &= 2a - \sqrt{ (x-1)^2 + y^2 } \\
\implies (x+1)^2 + y^2 &= 4a^2 +(x-1)^2 + y^2 - 4a\sqrt{ (x-1)^2 + y^2 } \\
\implies (x+1+x-1)(x+1-x+1)&= 4a^2 - 4a \sqrt{ (x-1)^2 + y^2 } \\
\implies a\sqrt{ (x-1)^2 +y^2 } &= a^2 -x \\
\implies a^2[(x-1)^2 + y^2] &= a^4 + x^2 - 2a^2x \\
\implies a^2[x^2 + 1 -2x +y^2] &= a^4 +x^2 - 2a^2x \\
\implies a^2x^2 + a^2 + a^2y^2 &= a^4 + x^2 \\
\implies x^2 + 1 + y^2 &= a^2 + \frac{x^2}{a^2} \\
\implies x^2\left( \frac{1}{a^2} - 1 \right)-y^2 &= 1-a^2 \\
\implies x^2\left( \frac{1-a^2}{a^2} \right)-y^2 &= 1-a^2 \\
\implies \frac{x^2}{a^2} +\frac{y^2}{a^2 -1} &= 1 \\
\implies \frac{x}{a^2} + \frac{yy'}{a^2 - 1} &= 0 \\
\implies (x+yy')a^2-x&=0 \\
\implies a^2 = \frac{x}{x+yy'} &\text{ and }a^2 -1= -\frac{yy'}{x+yy'}. 
\end{align}$$
Substitute into the fourth last equation to get
$$
\begin{align}
x(x+yy')-\frac{y}{y'}(x+yy') &=1  \\
\implies xy'(x+yy')-y(x+yy') &= y' \\
\implies (x+yy')(xy'-y) &= y'.
\end{align}
$$
The last equation is the required differential equation.