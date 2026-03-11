---
tags:
  - info
  - books
  - college
  - differential_equations
---
# Setup
We consider a [[linear system of differential equations (general form)|linear system of differential equations]] of the form
$$\begin{align}
L_{1}x+L_{2}y &= f_{1}(t) \\
L_{3}x + L_{4}y &=f_{2}(t)
\end{align}$$
where
$$\begin{align}
L_{1} &\equiv a_{0}D^m + a_{1}D^{m-1}+\dots + a_{m-1}D+ a_{m} \\
L_{2} &\equiv b_{0}D^n+ b_{1}D^{n-1}+\dots + b_{b-1}D+ b_{n} \\
L_{3} &\equiv \alpha_{0}D^p + \alpha_{1}D^{p-1}+\dots + \alpha_{p-1}D+ \alpha_{p} \\
L_{4} &\equiv \beta_{0}D^q + \beta_{1}D^{q-1}+\dots + \beta_{q-1}D+ \beta_{q}
\end{align}$$
and $a$'s, $b$'s, $\alpha$'s and $\beta$'s are constants.

# Method
Apply $L_{4}$ to the first equation and $L_{2}$ to the second equation to obtain
$$\begin{align}
L_{4}L_{1}x+L_{4}L_{2}y &= L_{4}f_{1} \\
L_{2}L_{3}x + L_{2}L_{4}y &=L_{2}f_{2}.
\end{align}$$
Subtract the second equation from the first, after noting that $L_{4}L_{2}y=L_{2}L_{4}y$. We get
$$L_{4}L_{1}x - L_{2}L_{3}x = L_{4}f_{1} - L_{2}f_{2}$$
or
$$(L_{1}L_{4} -L_{2}L_{3})x = L_{4}f_{1}-L_{2}f_{2}.$$
We assume that the operator $L_{1}L_{4} -L_{2}L_{3}$ is not a constant (??) and assume that $f_{1}$ and $f_{2}$ are such that the rhs exists. Denote the rhs by some function of $t$, say $g$. Then the equation may be written as
$$L_{5}x = g_{1}.$$
Note that $y$ is eliminated, and the equation is a linear differential equation with constant coefficients. (see: [[Ordinary Differential Equations#Theory of linear equations of order $n$]] to solve this equation.)

Next apply $L_{3}$ and $L_{1}$ to the first and second equations and carry out a similar procedure to get the equation
$$L_{5}y =g_{2}.$$
