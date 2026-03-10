---
tags:
  - info
  - books
  - college
  - differential_equations
---
# Statement
Suppose $v$ is any solution of 
$$a_{0}(x)y^{(n)} + a_{1}(x)y^{(n-1)} + \dots + a_{n-1}(x)y' + a_{n}(x)y = F(x)$$
and suppose $u$ is any solution of
$$a_{0}(x)y^{(n)} + a_{1}(x)y^{(n-1)} + \dots + a_{n-1}(x)y' + a_{n}(x)y = 0.$$
Then, $u + v$ is also a solution of the first non-homogeneous equation.

# Developing the above statement

(Note the subtle difference between the first theorem and the theorem that follows!)

Let $y_{p}$ be a solution of the non-homogeneous linear equation that involves no arbitrary constants and let
$$y_{c} = c_{1}y_{1}+\dots + c_{n}y_{n}$$
be the general solution of the corresponding homogeneous equation. 

Then *every* solution $\phi$ of the non-homogeneous equation can be expressed in the form $y_{c}+y_{p}$, i.e., 
$$c_{1}y_{1} + \dots+ c_{n}y_{n} + y_{p}$$
where $c_{1},\dots,c_{n}$ are suitably chosen.