---
tags:
  - info
  - books
  - college
  - differential_equations
---
# Statement

Consider the differential equation
$$M(x,y)dx + N(x,y)dy=0$$
where $M$ and $N$ have *continuous first partial derivatives* at all points $(x,y)$ in a rectangular domain $D$.

The differential equation is an [[exact differential equation]] in $D$ iff
$$\frac{\partial M(x,y)}{\partial y}= \frac{\partial N(x,y)}{\partial x}$$for all $(x,y)\in D$.

# Proof
Suppose the differential equation is exact. Then $Mdx + Ndy$ is an exact differential in $D$, i.e., there exists a function $F$ such that
$$\frac{\partial F(x,y)}{\partial x}=M(x,y)$$
and
$$\frac{\partial F(x,y)}{\partial y}=N(x,y)$$
for all $(x,y)\in D$. Since $M$ and $N$ have partial derivatives in $D$, we have
$$\frac{\partial^2F(x,y)}{\partial y \partial x}= \frac{\partial M(x,y)}{\partial y}$$
and
$$\frac{\partial^2 F(x,y)}{\partial x\partial y} = \frac{\partial N(x,y)}{\partial x}$$
for all $(x,y) \in D$. Since the partial derivatives of $M$ and $N$ are also continuous, by Clairaut's theorem, we have
$$\frac{\partial^2F(x,y)}{\partial y \partial x} =\frac{\partial M(x,y)}{\partial y}=\frac{\partial N(x,y)}{\partial x}=\frac{\partial^2 F(x,y)}{\partial x\partial y}$$
for all $(x,y) \in D$.

Now suppose 
$$\frac{\partial M(x,y)}{\partial y}= \frac{\partial N(x,y)}{\partial x}$$for all $(x,y)\in D$.

**Claim:** The exact differential of
$$F(x,y) = \int M(x,y)\partial x + \int\left[ N(x,y) - \int \frac{\partial M(x,y)}{\partial y} \partial x\right]dy$$
is the lhs of $M(x,y)dx + N(x,y)dy$.

**Proof:**
Note that $F$ is of the form
$$F(x,y) = \int M(x,y)\partial x + \phi(y).$$
Differentiating partially with respect to $y$, we obtain
$$\frac{\partial F (x,y)}{\partial y} = \frac{\partial}{\partial y}\int M(x,y)\partial x + \frac{d\phi(y)}{dy}.$$

But
$$
\begin{align}
\frac{d\phi(y)}{dy}&= N(x,y) - \int \frac{\partial M(x,y)}{\partial y}\partial x \\
&= N(x,y) - \int \frac{\partial N(x,y)}{\partial x}\partial x \\
&= N(x,y) - N(x,y) \\
&= 0.
\end{align}
$$
Thus,
$$\begin{align}
\frac{\partial F(x,y)}{\partial y}
\end{align}$$


Since $\phi$ is a function of $y$ only, the derivative $\frac{d\phi}{dy}$ is also independent of $x$, and thus, 
$$\frac{\partial F(x,y)}{\partial y} -\frac{\partial}{\partial y}\int M(x,y)\partial x $$
must be independent of $x$.

Note that 
$$\frac{\partial}{\partial x}\left[ N(x,y) - \frac{\partial}{\partial y} \int M(x,y)\partial x \right] = \frac{\partial N(x,y)}{\partial x}- \frac{\partial^2}{\partial x\partial y}\int M(x,y)\partial x.$$
We must have
