---
tags:
  - college
  - differential_equations
  - info
---
# Solution of a differential equation

Consider the $n$th order ordinary differential equation:
$$F\left( x, y, \frac{dy}{dx},\dots, \frac{d^ny}{dx^n} \right)=0$$
where $F$ is a real function of its $n+2$ arguments $x,y, \frac{dy}{dx}, \frac{d^nx}{dx^n}$.

### Explicit Solution

Let $f$ be a real function defined for all $x$ in a real interval $I$ and having an $n$th derivative (and hence all lower ordered derivatives) for all $x \in I$.

The function $f$ is called an **explicit solution** of the differential equation on $I$ iff it fulfills the following: 

$F(x,f(x),f'(x), \dots, f^{(n)}(x))$ is defined for all $x \in I$ and is equal to $0$ for all $x \in I$.

### Implicit Solution

A relation $g(x,y)=0$ is called an **implicit solution** of the differential equation if this relation defines at least one real function $f$ of the variable $x$ on an interval $I$ such that this function is an explicit solution on $I$.

### Examples

The relation 
$$x^2 + y^2 - 25=0$$ is an implicit solution of the differential equation
$$x + y \frac{dy}{dx} = 0$$
on the interval $I$ defined by $-5 < x < 5$.

Note that the relation defines two real functions $f_{1}$ and $f_{2}$ that are given by
$$f_{1}(x) = \sqrt{ 25 - x^2 }$$
and
$$f_{2}(x) = -\sqrt{ 25 - x^2 }$$
for all $x \in I$.

We see that
$$f'_{1}(x) = -\frac{x}{\sqrt{ 25 - x^2 }}.$$
Substituting $f_{1}(x)$ for $y$ and $f'_{1}(x)$ for $\frac{dy}{dx}$ in the differential equation, the lhs becomes
$$x+ \sqrt{ 25-x^2 }\left(  -\frac{x}{\sqrt{ 25 - x^2 }} \right)=x - x$$
which is equal to the rhs for all $x \in I$. 

Thus $f_{1}$ is an explicit solution and hence the relation is an implicit solution of the differential equation.

### Formal Solution

Consider the relation 
$$x^2 + y^2 + 25 = 0.$$
Is this an implicit solution of the differential equation
$$x + y \frac{dy}{dx} = 0?$$
Let us differentiate the relation implicitly with respect to $x$. We obtain
$$2x + 2y \frac{dy}{dx}=0 \implies x = -y \frac{dy}{dx}.$$
Note that substituting this satisfies the differential equation.

But CANNOT conclude from here that the relation is an implicit solution.

This is a **formal solution**; it only has the *appearance* of having a solution.

Also note that the relation we considered yields non-real values of $y$ for real values of $x$ and thus does not define any real function. 