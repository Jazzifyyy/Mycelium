---
tags:
  - info
  - books
  - college
  - differential_equations
---
(See: [[uc functions and uc sets]])

We aim to find a particular solution $y_{p}$ of
$$a_{0}y^{(n)} + a_{1}y^{(n-1)}+\dots+a_{n}y = F(x)$$
where $F$ is a finite linear combination 
$$F = \sum_{i=1}^m A_{i}u_{m}$$
of UC functions $u_{1},\dots,u_{m}$ and $A_{i}$ being known constants.

Suppose the complementary function $y_{c}$ has already been obtained. Then

1. For each UC function $u_{1},\dots,u_{m}$, form the corresponding UC set to get $S_{1},\dots,S_{m}$.
2. If we get identical UC sets, or a UC set being a subset of another one, then omit the identical or smaller set from further consideration.
3. If one of the UC sets atleast one member which is a solution of the corresponding *homogeneous* equation, then multiply all the members of that set by the lowest positive integral power of $x$ so that the resulting set will contain no members that are solutions of the homogeneous equation. Replace that set by this revised set.
4. Form a linear combination of all the sets with arbitrary coefficients. Determine the coefficients by demanding that it satisfies the differential equation.