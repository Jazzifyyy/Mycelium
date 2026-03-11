---
tags:
  - info
  - books
  - college
  - differential_equations
---
# Statement
The transformation $x = e^t$ reduces the [[cauchy-euler equation]] to a linear differential equation with constant coefficients.
# Proof
We prove this for a second degree cauchy-euler equation:
$$a_{0}x^2 \frac{d^2y}{dx^2} + a_{1}x \frac{dy}{dx}+a_{2}y = F(x).$$
Assume $x>0$ and let $x=e^t$. Then $t = \ln x$ and
$$\frac{dy}{dx} = \frac{dy}{dt} \frac{dt}{dx} = \frac{1}{x} \frac{dy}{dt}$$
and
$$\begin{align}
\frac{d^2y}{dx^2} &= \frac{d}{dx}\left( \frac{dy}{dx} \right) \\
&= \frac{d}{dx}\left( \frac{1}{x} \frac{dy}{dt} \right) \\

\end{align}$$