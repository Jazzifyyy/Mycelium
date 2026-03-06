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
ex