---
tags:
  - info
  - books
  - college
  - differential_equations
---
# Distinct real roots

Suppose 
$$a_{0}y^{(n)} + a_{1}y^{(n-1)} + \dots + a_{n-1}y' + a_{n}y = 0$$
has an [[auxiliary or characteristic equation of differential equation|auxiliary equation]] that has $n$ distinct real roots $m_{1},\dots,m_{n}$. Then the general solution of the differential equation is 
$$y = c_{1}e^{m_{1}x}+\dots+ c_{n}e^{m_{n}x}$$
where $c_{1},\dots,c_{n}$ are abitrary constants.

# Repeated real roots

Suppose 
$$a_{0}y^{(n)} + a_{1}y^{(n-1)} + \dots + a_{n-1}y' + a_{n}y = 0$$
has an [[auxiliary or characteristic equation of differential equation|auxiliary equation]] that has the real root $m$ occuring $k$ times, and the remaining roots are real numbers $m_{k+1},\dots,m_{n}$, then the general solution of the differential equation is
$$\begin{align}
y &= c_{1}e^{mx}+c_{2}xe^{mx}+c_{3}x^2e^{mx}+\dots+c_{k}x^{k-1}e^{mx}+c_{k+1}e^{m_{k+1}x}+\dots+c_{n}e^{m_{n}x} \\
&= (c_{1}+c_{2}x+\dots+c_{k}x^{k-1})e^{mx} + c_{k+1}e^{m_{k+1}x}+\dots + c_{n}e^{m_{n}x}.
\end{align}$$