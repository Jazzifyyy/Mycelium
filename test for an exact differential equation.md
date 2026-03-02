---
tags:
  - info
  - books
  - college
  - differential_equations
---
# Statement

Consider the differential equation
$$M(x,y)dx + N(x,y)dy=0$$
where $M$ and $N$ have continuous first partial derivatives at all points $(x,y)$ in a rectangular domain $D$.

The differential equation is an [[exact differential equation]] in $D$ iff
$$\frac{\partial M(x,y)}{\partial y}= \frac{\partial N(x,y)}{\partial x}$$for all $(x,y)\in D$.

# Proof
Suppose the differential equation is exact. Then $Mdx + Ndy$ is an exact differential in $D$, i.e., there exists a function $F$ such that
$$\frac{\partial F(x,y)}{\partial x}=M(x,y)$$
and
$$\frac{\partial F(x,y)}{\partial y}$$