---
tags:
  - info
  - books
  - college
  - differential_equations
---
# Statement
Suppose $n \neq 0$ or $1$. Then the transformation $v = y^{1-n}$ reduces a [[bernoulli differential equation]] to a linear equation in $v$.

# Proof
Multiply by $y^{-n}$ to get
$$y^{-n} \frac{dy}{dx} + P(x)y^{1-n} = Q(x).$$
Let $v = y^{1-n}$ to get, by chain rule, that
$$\frac{dv}{dx} = (1-n)y^{-n} \frac{dy}{dx}.$$
Substitute in the first equation to get
$$\frac{1}{1-n} \frac{dv}{dx} + P(x)v = Q(x)$$