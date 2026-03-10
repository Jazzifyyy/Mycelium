---
tags:
  - info
  - college
  - books
  - differential_equations
---
# Definition
Suppose $f_{1},\dots,f_{n}$ are $n$ real functions each of which has an $(n-1)$ derivative on $[a,b]$. The determinant
$$W(f_{1},\dots,f_{n}) = \begin{vmatrix}
f_{1} & \dots & f_{n} \\
f_{1}' & \dots & f_{n}' \\
\vdots & \ddots & \vdots \\
f_{1}^{(n-1)} & \dots & f_{n}^{(n-1)}
\end{vmatrix}$$
is called the **Wronskian** of these $n$ functions. 

Note that $W$ is itself a function defined on $[a,b]$ and its value at $x$ is denoted by $W(f_{1},\dots,f_{n})(x)$ or by $W[f_{1}(x), \dots, f_{n}(x)]$.