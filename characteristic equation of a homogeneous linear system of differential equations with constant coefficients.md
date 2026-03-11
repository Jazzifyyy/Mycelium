---
tags:
  - info
  - books
  - college
  - differential_equations
---
# Motivation
Consider [[homogeneous linear systems with constant coefficients - two equation in two unknown functions]].

Let us attempt to determine a solution of the form
$$\begin{align}
x &= A e ^{\lambda t}, \\
y &= B e ^{\lambda t}.
\end{align}$$
If we substitue them into the system, we must have
$$\begin{align}
(a_{1}-\lambda)A + b_{1}B &= 0 \\
a_{2}A + (b_{2} - \lambda)B&= 0.
\end{align}$$
A necessary and sufficient condition that this system has a non-trivial solution is:
$$\begin{vmatrix}
a_{1}-\lambda & b_{1} \\
a_{2} & b_{2}  - \lambda
\end{vmatrix} = 0.$$
Expanding this out we are led to the following characteristic equation.
# Definition
The **characteristic equation** of 
$$\begin{align}
x' &= a_{1}x+ b_{1}y \\
y' &= a_{2}x + b_{2}y
\end{align}$$
is given by
$$\lambda^2 - (a_{1}+b_{2})\lambda + (a_{1}b_{2} - a_{2}b_{1})=0.$$
