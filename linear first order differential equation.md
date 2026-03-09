---
tags:
  - info
  - books
  - college
  - differential_equations
---
# Definition
A [[first-order differential equation]] is **linear** in the dependent variable $y$ and the independent variable $x$ if it is of the form
$$\frac{dy}{dx} + P(x)y = Q(x).$$
# Is this exact?
Rewrite:
$$[P(x)y - Q(x)]dx + dy =0.$$
The above equation is of the form
$$M(x,y)dx + N(x,y)dy=0$$
where $M(x,y)= P(x)y - Q(x)$ and $N(x,y)=1$.

Note that 
$$\frac{\partial M(x,y)}{\partial y}=P(x)$$
and
$$\frac{\partial N(x,y)}{\partial x}=0.$$
Thus the original equation is not exact uncless $P(x)=0$, in which case the original equation turns into a simple separable equation.

If $P(x)=0$, it may be noted that the original equation possesses an [[integrating factor of an inexact differential equation|integrating factor]] that depends on $x$ only and may easily be found. Multiply the equation by $\mu(x)$ to obtain:
$$[\mu(x)P(x)y - \mu(x)Q(x)]dx + \mu(x)dy=0.$$
Note that $\mu(x)$ is an integrating factor iff

$$\frac{\partial}{\partial y}[\mu(x)P(x)y - \mu(x)Q(x)] = \frac{\partial}{\partial x}[\mu(x)],$$
i.e., iff
$$\mu(x)P(x) = \frac{d}{dx}[\mu(x)].$$
Note that $\mu$ is an unknown function of $x$ that we are trying to determine. Rewrite above as
$$\mu P(x) = \frac{d\mu}{dx},$$
i.e., 
$$\frac{d\mu}{\mu} = P(x)dx.$$
Integrate:
$$\ln|\mu | = \int P(x)dx$$
or 
$$\mu(x) = e^{\int P(x)dx}.$$
