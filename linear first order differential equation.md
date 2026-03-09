---
tags:
  - info
  - books
  - college
  - differential_equations
---
# Definition
A [[first-order differential equation]] is **linear** in the dependent variable $y$ and the independent variable $x$ if it is of the form
$$\frac{dy}{dx} + P(x)y = Q(x).$$
# Is this exact?
Rewrite:
$$[P(x)y - Q(x)]dx + dy =0.$$
The above equation is of the form
$$M(x,y)dx + N(x,y)dy=0$$
where $M(x,y)= P(x)y - Q(x)$ and $N(x,y)=1$.

Note that 
$$\frac{\partial M(x,y)}{\partial y}=P(x)$$
and
$$\frac{\partial N(x,y)}{\partial x}=0.$$
Thus the original equation is not exact uncless $P(x)=0$, in which case the original equation turns into a simple separable equation.