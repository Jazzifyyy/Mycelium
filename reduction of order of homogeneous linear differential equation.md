---
tags:
  - info
  - books
  - college
  - differential_equations
---
# Statement
Suppose $f$ is a non-trivial (non-zero) solution of 
$$a_{0}(x)y^{(n)} + a_{1}(x)y^{(n-1)} + \dots + a_{n-1}(x)y' + a_{n}(x)y = 0,$$
then the transformation $y = f(x)v$ reduces this equation to an $(n-1)$th order homogeneous linear differential equation in the dependent variable $w = \frac{dv}{dx}$.

# Let's look at the $n=2$ case!
Suppose $f$ is a known non-trivial solution of the second-order homogeneous linear equation
$$a_{0}(x)y'' + a_{1}(x)y' + a_{2}(x)y = 0.$$
Tranform $y = f(x)v$ where $v$ is a function of $x$ that will be determined. By chain rule, we have
$$y' = f(x)v' + f'(x)v$$
and
$$y'' = f(x)v'' + 2 f'(x)v' + f''(x)v.$$
Substituting the above two in the main equation, we obtain
$$a_{0}(x)[f(x)v'' + 2f'(x)v' + f''(x)v] + a_{1}(x)[f(x)v' + f'(x)v]+ a_{2}(x)f(x)v=0$$
or
$$a_{0}(x)f(x)v'' + [2a_{0}(x)f'(x)+a_{1}(x)f(x)]v'+ [a_{0}(x)f''(x)+a_{1}f'(x)+a_{2}(x)f(x)]v $$