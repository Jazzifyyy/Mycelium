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
Since this is exact, the one-parameter family of solutions of this differential equation is given by $F(x,y)=c$, where $F$ is a function such that 
$$\frac{\partial F(x,y)}{\partial x} = M(x)$$
and 
$$\frac{\partial F(x,y)}{\partial y}=N(y)$$
for all $(x,y)\in D$.

It follows that the one-parameter family of solutions is
$$\int M(x)dx + \int N(y)dy=c.$$
## Note
We must also investigate the possible loss or gain of solutions that may have occurred when multiplied with $\frac{1}{f(x)G(y)}$. (note the tacit assumption that neither $f(x)$ nor $G(y)$ is zero.)

Writing the original differential equation in derivative form, we have
$$f(x)g(y) \frac{dy}{dx} + F(x)G(y)=0,$$
where we regarded $y$ as the dependent variable.

Note that if $y_{0}$ is any real number such that $G(y_{0})=0$, then $y=y_{0}$ is a contant solution of the original differential equation; and this solution may have been lost in the separation process.

Thus, first we should always make the assumption that any factors by which we divide in the separation process is not zero. Then we must find the 