---
tags:
  - info
  - books
  - college
  - differential_equations
---
# Statement
The transformation $x = e^t$ reduces the [[cauchy-euler equation]] to a linear differential equation with *constant* coefficients.
# Proof
We prove this for a second degree cauchy-euler equation:
$$a_{0}x^2 \frac{d^2y}{dx^2} + a_{1}x \frac{dy}{dx}+a_{2}y = F(x).$$
Assume $x>0$ and let $x=e^t$. Then $t = \ln x$ and
$$\frac{dy}{dx} = \frac{dy}{dt} \frac{dt}{dx} = \frac{1}{x} \frac{dy}{dt}$$
and
$$\begin{align}
\frac{d^2y}{dx^2} &= \frac{1}{x} \frac{d}{dx}\left( \frac{dy}{dt} \right) + \frac{dy}{dt} \frac{d}{dx} \left( \frac{1}{x} \right) \\
&= \frac{1}{x} \left( \frac{d^2y}{dt} \frac{dt}{dx} \right) - \frac{1}{x^2} \frac{dy}{dt} \\
&= \frac{1}{x}\left(  \frac{d^2y}{dt} \frac{1}{x} \right) - \frac{1}{x^2} \frac{dy}{dt} \\
&= \frac{1}{x^2} \left( \frac{d^2y}{dt^2} - \frac{dy}{dt} \right).
\end{align}$$
Thus, we see that 
$$x \frac{dy}{dx} = \frac{dy}{dt}$$
and 
$$x^2 \frac{d^2y}{dx^2} = \frac{d^2y}{dt^2} - \frac{dy}{dt}.$$
Substitute to get
$$a_{0}\left(\frac{d^2y}{dt^2} - \frac{dy}{dt}\right) + a_{1}\left(  \frac{dy}{dt} \right) + a_{2}y = F(e^t).$$
This is of the form
$$A_{0} \frac{d^2y}{dt^2} + A_{1} \frac{dy}{dt} + A_{2}y = G(t)$$
which is a second-order linear differential equation with *constant* coefficients.
