---
tags:
  - info
  - books
  - college
  - differential_equations
---
# Definition
If the differential equation 
$$M(x,y)dx + N(x,y)dy=0$$
is NOT an [[exact differential equation]] in domain $D$ but the differential equation 
$$\mu(x,y)M(x,y)dx + \mu(x,y)N(x,y)dy=0$$
is exact in $D$, then $\mu(x,y)$ is called an **integrating factor** of the first differential equation.

## Note

The multiplication of the original equation by the integrating factor may result in either 
1. the loss of one or more solutions of the original; or
2. the gain of one or more functions which are solutions of the new equation but *not* of the original equation; or
3. both of the above.

# Example
The differential equation
$$(3y + 4xy^2 )dx + (2x + 3x^2y)dy=0$$
is not exact:
$$\frac{\partial M(x,y)}{\partial y}= 3 + 8xy \neq 2+6xy = \frac{\partial M(x,y)}{\partial x}$$
except for $(x,y)$ such that $2xy + 1=0$, i.e., the equation is not exact in any rectangular domain.

Define $\mu(x,y)=x^2y$ and multiply it on both sides of the equation to get
$$(3x^2y^2+4x^3y^3)dx + (2x^3y +3x^4y^2)dy=0.$$
This equation is exact in every rectangular domain: 
$$\frac{\partial \mu(x,y)M(x,y)}{\partial y}=6x^2y + 12x^3y^2 + \frac{\partial \mu(x,y)N(x,y)}{\partial x}$$
for all real $(x,y)$.

Thus, $x^2y$ is an integrating factor.
