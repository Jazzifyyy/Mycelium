---
tags:
  - info
  - books
  - college
  - differential_equations
---
# Statement
If 
$$M(x,y)dx + N(x, y)dy=0$$
is a [[homogeneous equation]], then the change of variables $y = vx$ transforms the equation into a [[separable equation]] in the variables $v$ and $x$.
# Proof

Since the equation is homogeneous, it may be written in the form
$$\frac{dy}{dx} = g\left( \frac{y}{x} \right).$$
Let $y=vx$. Then by the chain rule,
$$\frac{dy}{dx} = v + x\frac{dv}{dx}$$
and thus, 
$$v + x \frac{dv}{dx} = g(v)$$
or 
$$[v - g(v)]dx + xdv =0.$$
This equation is separable. Dividing by $[v-g(v)]x$, we obtain
$$dx + $$