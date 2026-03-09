---
tags:
  - info
  - books
  - college
  - differential_equations
---
A [[linear first order differential equation]] has an [[integrating factor of an inexact differential equation|integrating factor]] $e^{\int P(x)dx}$.

To find the solution of the differential equation, we employ a simple approch: multiply both sides of the equation in its derivative form by the IF to obtain
$$e^{\int P(x)dx} \frac{dy}{dx} + e^{\int P(x)dx} P(x)y = Q(x)e^{\int P(x)dx}$$
i.e.,

$$\frac{d}{dx}\left[ e^{\int P(x)dx}y \right] = Q(x)e^{\int P(x)dx}.$$
Integrating,
$$e^{\int P(x)dx}y = \int e^{\int P(x)dx}Q(x)dx +c;$$
i.e., a one-parameter family of solutions is
$$y = \frac{1}{e^{\int P(x)dx}}\left[\int e^{\int P(x)dx}Q(x)dx +c\right].$$

Furthermore, it can be shown that this one-parameter family of solutions includes *all* the solutions of the equation.

# Examples
## Example 1
Consider the differential equation
$$y^2 dx + (3xy -1)dy = 0.$$
This becomes
$$\frac{dy}{dx} = \frac{y^2}{1 - 3xy}$$
which is not linear in $y$, not exact, not separabe, nor homogeneous.

It appears to be of a type that we have not yet encountered; but note that in the differential form of a first-order differential equation, the roles of $x$ and $y$ are interchangeable, in the sense that either variable may be regarded as the dependent variable and the other as the independent variable. 

So let us now regard $x$ as the dependent variable and $y$ as the independent variable. With this, we have
$$\frac{dx}{dy} = \frac{1-3xy}{y^2}$$
i.e.,
$$\frac{dx}{dy} + \frac{3}{y}x = \frac{1}{y^2}.$$
This is of the form
$$\frac{dx}{dy} + P(y)x = Q(y).$$
Thus the theory developed here may be applied to this equation merely by interchanging the roles of $x$ and $y$.