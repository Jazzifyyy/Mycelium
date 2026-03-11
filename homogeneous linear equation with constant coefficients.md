---
tags:
  - info
  - books
  - college
  - differential_equations
---
We wish to solve
$$a_{0}y^{(n)} + a_{1}y^{(n-1)} + \dots + a_{n-1}y' + a_{n}y = 0$$
where $a_{0},\dots,a_{n}$ are constants instead of functions. 

Can we try and guess a solution of this equation? Maybe if we had a function $f$ such that 
$$\frac{d^k}{dx^k}f(x)=cf(x).$$
Such a function is $y=e^{mx}$, where $m$ is chosen such that the equation is true. Note that
$$y^{(k)} = m^k e^{mx}.$$
If $y = e^{mx}$ is indeed a solution, then 
$$e^{mx}(a_{0}m^n +\dots+a_{n})=0.$$
Since $e^{mx} \neq 0$, the [[auxiliary or characteristic equation of differential equation|auxiliary equation]] holds for $m$.