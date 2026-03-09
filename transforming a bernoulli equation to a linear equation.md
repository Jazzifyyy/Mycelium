---
tags:
  - info
  - books
  - college
  - differential_equations
---
# Statement
Suppose $n \neq 0$ or $1$. Then the transformation $v = y^{1-n}$ reduces a [[bernoulli differential equation]] to a [[linear first order differential equation]] in $v$.

# Proof
Multiply by $y^{-n}$ to get
$$y^{-n} \frac{dy}{dx} + P(x)y^{1-n} = Q(x).$$
Let $v = y^{1-n}$ to get, by chain rule, that
$$\frac{dv}{dx} = (1-n)y^{-n} \frac{dy}{dx}.$$
Substitute in the first equation to get
$$\frac{1}{1-n} \frac{dv}{dx} + P(x)v = Q(x)$$
or
$$\frac{dv}{dx} + (1-n)P(x)v = (1-n)Q(x).$$
Let $P_{1}(x) = (1-n)P(x)$ and $Q_{1}(x) = (1-n)Q(x)$
and this may be written as 
$$\frac{dv}{dx} + P_{1}(x)v = Q_{1}(x)$$
which is linear in $v$.

# Example
(...)