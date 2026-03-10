---
tags:
  - info
  - college
  - books
  - differential_equations
---
# Newton's second law
The rate of change of momentum of a body is proportional to the resultant force acting on the body and is in the directon of this resultant force, i.e., 
$$\frac{d}{dt}(mv) = KF$$
where $m$ is the mass of the body, $v$ is its velocity, $F$ is the resultant force acting upon it, and $K$ is a constant of proportionality.

Suppose $m$ is constant, then
$$\begin{align}
m \frac{dv}{dt} &= KF \\
\implies a &= K \frac{F}{m} \\
\implies F &= kma\\
\end{align}$$
where $k = \frac{1}{K}$ and $a = \frac{dv}{dt}$. Also, $k$ depends on the units employed for force, mass, and acceleartion. Upon choosing a system of units for which $k=1$, we have
$$F=ma.$$
Consider a body in rectilinear motion, then the second law may be expresses in any of the following forms:
$$\begin{align}
m \frac{dv}{dt} &= F, \\
m \frac{d^2x}{dt^2} &= F, \\
mv \frac{dv}{dx}&=F
\end{align}$$
where $F$ is the resultartn force acting on the body.

# Examples
## Example 1

A body weighing $8$ lb falls from rest toward the earth from a great height. As it falls, air resistance acts upon it, and we assume that this resistance (in pounds) is numerically equal to $2v$, where $v$ is the velocity (in feet per second). Find the velocity and distance fallen at time $t$ seconds. 

**Formulation:** positive x axis: downward. Origin: The point from which the body fell. Then
1. $F_{1} = 8$ lb is the body's weight; and
2. $F_{2} = -2v$ is the air resistance.

By Newton's second law, we have
$$m \frac{dv}{dt} = F_{1} + F_{2}.$$
We have $g = 32$ and $m = \frac{w}{g} = \frac{8}{32} = \frac{1}{4}$. This yields:
$$\frac{1}{4} \frac{dv}{dt} = 8 - 2v.$$
Since the body was initially at rest, we have the initial condition
$$v(0)=0.$$
### Solution

The differential equation is separable. Separating the variables, we have
$$\frac{dv}{8 - 2v} = 4dt.$$
Integrate:
$$-\frac{1}{2} \ln|8 - 2v| = 4t + c_{0}$$
i.e., 
$$8 - 2v = c_{1}e^{ -8t }.$$
The initial condition gives us $c_{1}=8$. Thus the velocity at time $t$ is given by
$$v = 4(1-e^{-8t}).$$
To determine the distance fallen at time $t$, write the above equation in the form
$$\frac{dx}{dt} = 4(1- e^{-8t})$$
with the initial condition $x(0)=0$.

Integrate the above equation:
$$x = t\left( t + \frac{1}{8}e^{-8t} \right) + c_{2}.$$
The initial conidition gives us $c_{2} = -\frac{1}{2}$ and hence the distance fallen is given by
$$x = 4\left( t + \frac{1}{8}e^{-8t} - \frac{1}{8} \right).$$
