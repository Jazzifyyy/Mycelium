---
tags:
  - info
  - books
  - college
  - differential_equations
---
# Definition
An equation of the form
$$F(x)G(y)dx + f(x)g(y)dy=0$$
is called a **separable equation**.

For example, the equation $(x-4)y^4dx - x^3(y^2 - 3)dy =0$ is a separable equation.

# Motivation
In general, a separable equation is not exact, but it possesses an obvious integrating factor, namely $\frac{1}{f(x)G(y)}$. For if we multiply the seperable equation by this expression, we get
$$\frac{F(x)}{f(x)}dx + \frac{g(y)}{G(y)}dy=0.$$
Note that this equation is exact, since
$$\frac{\partial }{\partial y}\left[ \frac{F(x)}{f(x)} \right]= 0 = \frac{\partial}{\partial x}\left[ \frac{g(y)}{G(y)} \right].$$
Further note that upon the multiplication of $\frac{1}{f(x)G(y)}$ with the separable equation, we get
$$M(x)dx + N(y)dy=0.$$
