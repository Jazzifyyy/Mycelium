---
tags:
  - info
  - books
  - college
  - differential_equations
---
We develop this method in context of second-order linear differential equations
$$a_{0}(x)y''+a_{1}(x)y' + a_{2}(x)y = F(x).$$
Suppose $y_{1}$ and $y_{2}$ are linearly independent solutions of 
$$a_{0}(x)y''+a_{1}(x)y' + a_{2}(x)y = 0.$$
Then the general solution for this equation is of the form $c_{1}y_{1}(x)+c_{2}y_{2}(x)$.

We wish to find functions $v_{1}$ and $v_{2}$ such that $v_{1}(x)y_{1}(x)+v_{2}(x)y_{2}(x)$ is a particular solution of the non-homogeneous equation.

(Note that we have two functions but only one condition (that is a solution of the equation), we are thus free to impose another condition.)

Write 
$$y_{p} = v_{1}(x)y_{1}(x)+v_{2}(x)y_{2}(x).$$
Differentiating, we have
$$y'_{p}(x) = v_{1}(x)y_{1}'(x) + v_{2}(x)y_{2}'(x)+v_{1}'(x)y_{1}(x)+v_{2}'(x)y_{2}(x).$$
Condition: $$v_{1}'(x)y_{1}(x)+v_{2}'(x)y_{2}(x)=0.$$
Then,
$$y'_{p}(x) = v_{1}(x)y_{1}'(x) + v_{2}(x)y_{2}'(x).$$
Differentiating, we have
$$y''_{p}(x) = v_{1}(x)y_{1}''(x)+v_{2}(x)y''_{2}(x)+v_{1}'(x)y_{1}'(x)+v_{2}'(x)y$$