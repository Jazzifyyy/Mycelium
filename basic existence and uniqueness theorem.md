---
tags:
  - info
  - books
  - differential_equations
---
# Statement
Consider the differential equation
$$\frac{dy}{dx} = f(x,y)$$
where 
1. the function $f$ is a continuous function of $x$ and $y$ in some domain $D$ of the $xy$ plane, and
2. The partial derivative $\frac{\partial f}{\partial y}$ is also a continuous function of $x$ and $y$ in $D$; and let $(x_{0},y_{0})$ be a point in $D$.

Then there exists a *unique* solution $\phi$ of the differential equation, defined on some interval $|x- x_{0}|\leq h$, where $h$ is sufficiently small, that satisfies the condition 
$$\phi(x_{0})=y_{0}.$$
# Examples
## Example 1

Consider
$$\frac{dy}{dx} = \frac{y}{\sqrt{ x }}$$
with $y(1)=2$.

We have
$$\frac{\partial f(x,y)}{\partial y} = \frac{1}{\sqrt{ x }}.$$
This is continuous in some $D$