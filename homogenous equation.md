---
tags:
  - info
  - college
  - books
  - differential_equations
---
# Definition
A [[first-order differential equation]] $M(x,y)dx + N(x,y)dy=0$ is said to be **homogeneous** if, when written in the derivative form $\frac{dy}{dx} = f(x,y)$, there exists a function $g$ such that $f(x,y)$ can be expressed in the form $g\left( \frac{y}{x} \right)$.

# Examples
## Example 1

The equation
$$(x^2 - 3y^2)dx + 2xydy=0$$
is homogeneous:

In derivative form,
$$\frac{dy}{dx} = \frac{3y^2 - x^2}{2xy}= \frac{3y}{2x} - \frac{x}{2y}  = \frac{3}{2}\left( \frac{y}{x} \right) - \frac{1}{2}\left( \frac{1}{y/x} \right).$$
## Example 2

The equation 
$$(y + \sqrt{ x^2 + y^2 })dx - xdy=0$$
is homogeneousL 

In derivative form,
$$\frac{dy}{dx} = \frac{y + \sqrt{ x^2 + y^2 }}{x}= \frac{y}{x} \pm \frac{\sqrt{ x^2 + y^2 }}{\sqrt{ x^2 }} = \frac{y}{x} \pm \sqrt{ 1 + \left( \frac{y}{x} \right)^2 }$$
depending on the sign of 
