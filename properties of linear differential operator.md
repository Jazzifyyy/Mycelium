---
tags:
  - info
  - books
  - college
  - differential_equations
---
Let $L$ denote the linear differential operator, i.e., 
$$L \equiv a_{0}D^n + a_{1}D^{n-1}+\dots + a_{n-1}D+ a_{n}$$
# Properties
## Property 1

Suppose $f_{1}$ and $f_{2}$ are both $n$ times differentiable functions of $t$ and $c_{1}$ and $c_{2}$ are constants. Then
$$L[c_{1}f_{1}+c_{2}f_{2}] = c_{1}L[f_{1}]+c_{2}L[f_{2}].$$

## Property 2

Let 
$$L_{1} \equiv a_{0}D^m + a_{1}D^{m-1}+\dots + a_{n-1}D+ a_{m}$$
and
$$L_{2} \equiv b_{0}D^n + b_{1}D^{n-1}+\dots + b_{n-1}D+ b_{n}$$
be two linear differential operators. 

Let 
$$L_{1}(r) \equiv a_{0}r^m + a_{1}r^{m-1}+\dots + a_{n-1}r+ a_{m}$$
and
$$L_{2}(r) \equiv b_{0}r^n + b_{1}r^{m-1}+\dots + b_{n-1}r+ b_{n}$$
be the polynomials obtained after replacing $D^k$ by $r^k$ from the respective operators. 

Define 
$$L(r)=L_{1}(r)L_{2}(r).$$
Then if $f$ is a function with $n+m$ derivatives, then 
$$L_{1}L_{2}f=L_{2}L_{1}f = Lf.$$
### Example of property 2

Let $L_{1} = D^2 + 1$ and $L_{2} = 3D + 2$ and $f(t)=t^3$. Then
$$\begin{align}
L_{1}L_{2}f &= (D^2+1)(3D+2)t^3 \\
&= (D^2 + 1)(9t^2+2t^3) \\
&= 
\end{align}$$