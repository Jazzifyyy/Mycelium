---
tags:
  - info
  - differential_equations
  - college
---
# Statement

Consider the differential equation
$$M(x,y)dx + N(x,y)dy=0$$
where $M$ and $N$ have *continuous first partial derivatives* at all points $(x,y)$ in a rectangular domain $D$ and suppose it is an [[exact differential equation]] in $D$. 

Then a one-parameter family of solutions of this differential equation is given by $F(x,y)=c$, where $F$ is a function such that 
$$\frac{\partial F(x,y)}{\partial x} = M(x,y)$$
and 
$$\frac{\partial F(x,y)}{\partial y}=N(x,y)$$
for all $(x,y)\in D$.

# Example
## Example 1

Solve the equation 
$$(3x^2+4xy)dx + (2x^2+2y)dy=0.$$
### Example 1 solution

We first need to determine whether the equation is exact or not. We have
$$\frac{\partial M(x,y)}{\partial y} = 4x = \frac{\partial N(x,y)}{\partial x}$$
for all $(x,y)$, and so is exact in every rectangular domain $D$.

Now we must find a function $F$ such that
$$\frac{\partial F(x,y)}{\partial x}=M(x,y)=3x^2 + 4xy$$
and
$$\frac{\partial F(x,y)}{\partial y} = N(x,y) = 2x^2 + 2y.$$
From the first equation, we have
$$$$