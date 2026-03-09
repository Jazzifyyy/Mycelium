---
tags:
  - info
  - books
  - college
  - differential_equations
---
# Problem
Solve the equation
$$(x^2 - 3y^2)dx + 2xy dy = 0.$$
From [[homogeneous equation#Example 1]], we know that this is a [[homogeneous equation]].  

By theorem "[[a homogeneous equation is separable]]" we know that the equation is separable.We let $y=vx$ to get
$$v + x \frac{dv}{dx} = -\frac{1}{2v} + \frac{3v}{2}$$
or
$$x \frac{dv}{dx} = -\frac{1}{2v} + \frac{v}{2}$$
or
$$x \frac{dv}{dx} = \frac{v^2 -1}{2v}.$$
This is separable. Separating the variables, we obtain
$$\frac{2vdv}{v^2 - 1}= \frac{dx}{x}.$$
Integrating,
$$\ln|v^2 - 1| = \ln|x| + \ln|c| $$
and thus
$$|v^2 -1| = |cx|.$$
Check that no solutions were lost in the separation process. Now, 