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

Thus, first we should always make the assumption that any factors by which we divide in the separation process is not zero. Then we must find the solutions $y=y_{0}$ of the equation $G(y)=0$ and determine whether any of these are solutions of the original equation which were lost in the separation process. 

# Example
## Example 1

Solve the equation $(x-4)y^4dx - x^3(y^2-3)dy=0$.

The equation is separable; separating the variables by dividing by $x^3y^4$, we obtain
$$\frac{(x-4)dx}{x^3} - \frac{(y^2-3)dy}{y^4}=0$$
or
$$(x^{-2} - 4x^{-3})dx - (y^{-2}-3y^{-4})dy=0.$$
Integrating, we have the one-parameter family of solutions
$$-\frac{1}{x} + \frac{2}{x^2} + \frac{1}{y} - \frac{1}{y^3}=c.$$
Note that on dividing by $x^3y^4$ in the separation process, we assumed that $x^3\neq0$ *and* $y^4 \neq 0$. Consider the solution $y=0$ of $y^4=0$. (Note that it is not a member of the one-parameter family of solutions which we obtained.) 

Writing the original differential equation in the derivative form:
$$\frac{dy}{dx} = \frac{(x-4)y^4}{x^3(y^2-3)}.$$
It is clear that $y=0$ is a solution of the original equation (and it was lost in the separation process).

## Example 2

Solve the initial-value problem that consists of the differential equation
$$x \sin y dx  + (x^2 + 1)\cos ydy =0$$
and the initial condition
$$y(1) = \frac{\pi}{2}.$$
This is a separable equation. Divide by $(x^2+1)\sin y$ to get
$$\frac{x}{x^2 + 1}dx + \frac{\cos y }{\sin y}dy=0.$$
Thus, the family of solutions is given by
$$\int \frac{xdx}{x^2 + 1} + \int \frac{\cos y}{\sin y}dy = c_{0}$$
or
$$\frac{1}{2}\ln (x^2 + 1) + \ln |\sin y| = c_{0}$$
or
$$\ln(x^2 + 1) + \ln \sin^2y=2\ln|c_{1}|=\ln c$$
or
$$\ln(x^2 + 1)\sin^2 y = \ln c$$
or
$$(x^2 + 1)\sin^2y = c.$$


