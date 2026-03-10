---
tags:
  - info
  - books
  - college
  - differential_equations
---
# Statement
Suppose $f$ is a non-trivial (non-zero) solution of 
$$a_{0}(x)y'' + a_{1}(x)y' + a_{2}(x)y = 0.$$
then the transformation $y = f(x)v$, where $v$ is a function of $x$, reduces this equation to an $(n-1)$th order homogeneous linear differential equation in the dependent variable $w = \frac{dv}{dx}$:
$$a_{0}(x)f(x) \frac{dw}{dx} + [2a_{0}(x)f'(x)+a_{1}(x)f(x)]w = 0.$$

## Note 1
This helps us to determine another solution of the second-order equation, since the first order equation gives the solution
$$w = \frac{\exp\left( - \int \frac{a_{1}(x)}{a_{0}(x)}dx \right)}{[f(x)]^2}$$
and using this, we get 
$$v(x) = \int \frac{\exp\left( - \int \frac{a_{1}(x)}{a_{0}(x)}dx \right)}{[f(x)]^2}dx$$
and using this, we get the function $g$ defined by
$$g(x) = f(x) \int \frac{\exp\left( - \int \frac{a_{1}(x)}{a_{0}(x)}dx \right)}{[f(x)]^2}dx$$
which is another solution of the second-order equation.

## Note 2

(See: [[any solution of a linear homogeneous differential equation can be expressed as linear combination of its linearly independent solutions]])

The original known solution $f$ and the new solution $g$ are linearly indendent, and hence the general solution of the second-order equation may be expressed as
$$c_{1}f+c_{2}g.$$

# Proof

Suppose $f$ is a known non-trivial solution of the second-order homogeneous linear equation
$$a_{0}(x)y'' + a_{1}(x)y' + a_{2}(x)y = 0.$$
Tranform $y = f(x)v$ where $v$ is a function of $x$ that will be determined. By chain rule, we have
$$y' = f(x)v' + f'(x)v$$
and
$$y'' = f(x)v'' + 2 f'(x)v' + f''(x)v.$$
Substituting the above two in the main equation, we obtain
$$a_{0}(x)[f(x)v'' + 2f'(x)v' + f''(x)v] + a_{1}(x)[f(x)v' + f'(x)v]+ a_{2}(x)f(x)v=0$$
or
$$a_{0}(x)f(x)v'' + [2a_{0}(x)f'(x)+a_{1}(x)f(x)]v'+ [a_{0}(x)f''(x)+a_{1}f'(x)+a_{2}(x)f(x)]v =0$$
Note that since $f$ is a solution, the coefficient of $v$ is zero. Let $w=v'$:
$$a_{0}(x)f(x) \frac{dw}{dx} + [2a_{0}(x)f'(x)+a_{1}(x)f(x)]w = 0.$$
This is a first-order homogeneous linear differential equation in the dependent variable $w$ and is separable (note that the tranformation led us to a first-order linear homogeneous equation); thus, assuming $f(x) \neq 0$ and $a_{0}(x) \neq 0$, we have
$$\frac{dw}{w} = -\left[ 2 \frac{f'(x)}{f(x)} + \frac{a_{1}(x)}{a_{0}(x)} \right]dx.$$
Integrating, we obtain
$$\ln|w| = - \ln[f^2(x)] - \int\frac{a_{1}(x)}{a_{0}(x)}dx + \ln|c|$$
or
$$w = \frac{c \exp\left( - \int \frac{a_{1}(x)}{a_{0}(x)}dx \right)}{[f(x)]^2}.$$
Take the solution for which $c=1$, and note that $\frac{dv}{dx}=w$. Integrating again, we have
$$v = \int \frac{\exp \left[ - \int \frac{a_{1}(x)}{a_{0}(x)}dx \right]}{[f(x)]^2}dx.$$

Substituting this back in $y = f(x)v$, we have
$$y = f(x)\int \frac{\exp \left[ - \int \frac{a_{1}(x)}{a_{0}(x)}dx \right]}{[f(x)]^2}dx.$$
The rhs, denote it by $g$, is a solution of the second-order original differential equation.


(Recall: [[test of linear independence of the solutions of a linear homogeneous differential equation]])
Note that $f$ and $g$ are linearly independent, since
$$\begin{align}
W(f,g)(x) &= \begin{vmatrix}
f(x) & g(x) \\
f'(x) & g'(x)
\end{vmatrix} \\
&= \begin{vmatrix}
f(x) & f(x)v \\
f'(x) & f(x)v'+ f'(x) v
\end{vmatrix} \\
&= [f(x)]^2v'  \\
&= [f(x)]^2 \frac{\exp \left[ - \int \frac{a_{1}(x)}{a_{0}(x)}dx \right]}{[f(x)]^2} \\
&= \exp \left[ - \int \frac{a_{1}(x)}{a_{0}(x)}dx \right]  \\
&\neq 0.
\end{align}$$
Thus, the linear combination $c_{1}f+c_{2}g$ is the general solution of the second order equation.