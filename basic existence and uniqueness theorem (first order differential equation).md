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
Both $f$ and the partial derivative are continuous in some $D$ around $(1,2)$.

Since $(1,2) \in D$, we know that the problem has a unique solution defined in some sufficiently small interval around $x_{0}=1$.

## Example 2

Consider
$$\frac{dy}{dx} = \frac{y}{\sqrt{ x }}$$
with $y(0)=2$.

Once again, 
$$\frac{\partial f(x,y)}{\partial y} = \frac{1}{\sqrt{ x }}.$$
Note that at $(0,2)$, neither $f$ nor the partial derivative is continuous, i.e., the point cannot be included in a domain $D$ where the hypotheses are satisfied. 

Thus, we cannot conclude that problem 2 has a solution.