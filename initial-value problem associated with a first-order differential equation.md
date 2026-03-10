---
tags:
  - books
  - differential_equations
  - info
  - college
---
# Definition
Consider the first-order differential equation
$$\frac{dy}{dx} = f(x,y)$$
where $f$ is continuous function of $x$ and $y$ in some domain (open and connected) $D$ of the $xy$ plane.  

Let $(x_{0},y_{0})$ be a point in $D$.

The **initial-value problem** associated with the differential equation is find a solution $\phi$, defined on some real interval containing $x_{0}$ and satisfies the initial condition:
$$\phi(x_{0})=y_{0}.$$
# Example
Solve the initial-value problem:
$$\frac{dy}{dx} = -\frac{x}{y}$$
with $y(3)=4$ given that the differential equation has a one-parameter family of solutions which may be written in the form:
$$x^2 + y^2 =c.$$

Substituting $x=3$ and $y=4$ yields $c^2 = 25$.

Thus, 
$$y = \pm \sqrt{ 25 - x^2 }.$$
We need the positive sign so that $y$ yields $+4$ at $x=3$. Thus the function $f$ defined by 
$$f(x) = \sqrt{ 25 -x^2 }$$
where $-5 < x < 5$ is the solution of the problem. 

