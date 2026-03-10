---
tags:
  - info
  - books
  - college
  - differential_equations
---
# Definition
If $f_{1},\dots,f_{n}$ are $n$ linearly independent solutions of the $n$th order homogeneous linear differential equation
$$a_{0}(x)y^{(n)} + a_{1}(x)y^{(n-1)} + \dots + a_{n-1}(x)y' + a_{n}(x)y = 0$$
on $[a,b]$ (these solutions always exist, see [[existence of linearly independent solutions of a linear homogeneous differential equation]]), then the set $f_{1},\dots,f_{n}$ is called a **fundamental set of solutions** and the function $f$ defined by
$$f(x)=c_{1}f_{1}(x)+\dots+ c_{n}f_{n}(x)$$
where $x \in [a,b]$ and $c_{1},\dots,c_{n}$ are arbitrary constants, is called a **general solution** on $[a,b]$.

# In linear algebra terms:
The set of all solutions of the stated differential equation form a vector space of dimension $n$, of which any subset of $n$ linearly independent solutions is a basis, since [[any solution of a linear homogeneous differential equation can be expressed as linear combination of its linearly independent solutions]]. 