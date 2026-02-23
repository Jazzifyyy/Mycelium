---
tags:
  - college
  - info
  - linear_algebra
---
# When do we have a solution?

Can we always solve a system of linear equations? That is, can we always find a $\tilde{\theta}$ such that $A\tilde{\theta}= \mathbf{b}$?

Suppose $\tilde{\theta}$ is a solution. Then
$$\begin{align}
&A\tilde{\theta} = \mathbf{b} \\
\iff \theta_{1}&\mathbf{a}^{(1)}+ \dots + \theta_{d}\mathbf{a}^{(d)} = \mathbf{b}. 
\end{align}$$
Thus, a solution exists iff $\mathbf{b} \in \mathcal{C}(A)$.

# A method to check solvability
Steps:
1. Calculate $\text{rank}(A)$ and $\text{rank}(A:b)$. 
2. The system has a solution iff $\text{rank}(A) = \text{rank}(A:b)$.

Why this works? Recall that $\text{rank}(A)$ is the number of independent columns of $A$; and these independent columns form a basis for $\mathcal{C}(A)$.

Note that $\text{rank}(A:b)$ can only take two possible values: $\text{rank}(A)$ and $\text{rank}(A)+1$.

Now note that
$$\begin{align}
\mathbf{b} \in \mathcal{C}(A) &\iff \mathbf{b}\text{ is linearly dependent on the columns of }A \\
& \iff A:b \text{ has the same no. of independent columns as }A \\
& \iff \text{rank}(A:b) = \text{rank}(A). 
\end{align}$$

# When is the solution unique?
Suppose a solution to $A \tilde{\theta} = \mathbf{b}$ exists. It is unique iff the columns of $A$ are independent, i.e., when $A$ has full column rank.

**Proof:** Suppose we have two distinct solutions $(\theta_{1},\dots, \theta_{d}) \neq (\eta_{1},\dots,\eta_{d})$, i.e., we have
$$\theta_{1}\mathbf{a}^{(1)}+ \dots + \theta_{d}\mathbf{a}^{(d)} = \mathbf{b}$$
and
$$\eta_{1}\mathbf{a}^{(1)}+ \dots + \eta_{d}\mathbf{a}^{(d)} = \mathbf{b}.$$
This implies that
$$(\theta_{1}-\eta_{1})\mathbf{a}^{(1)} + \dots + (\theta_{d} - \eta_{d})\mathbf{a}^{(d)}=0.$$
But since the solutions were distinct, atleast one of the coefficients is non-zero. Thus, $\mathbf{a}^{(1)},\dots, \mathbf{a}^{(d)}$ are dependent.

Now suppose the columns of $A$ are dependent. Thus, there exists $c_{1},\dots,c_{d}$, not all zero, such that 
$$c_{1}\mathbf{a}^{(1)}+\dots + c_{d}\mathbf{a}^{(d)} = 0.$$ Also suppose that $(\theta_{1},\dots,\theta_{d})$ is a solution, i.e., 
$$\theta_{1}\mathbf{a}^{(1)} + \dots + \theta_{d}\mathbf{a}^{(d)} = \mathbf{b}.$$
Adding the two equations, we have
$$(\theta_{1}+c_{1})\mathbf{a}^{(1)} + \dots + (\theta_{d}+c_{d})\mathbf{a}^{(d)} = \mathbf{b}.$$
Thus, we have found another solution: $(\theta_{1}+c_{1}, \dots, \theta_{d}+c_{d})$ which is distinct from $(\theta_{1},\dots,\theta_{d})$.

# How to find the solution?
From now on, we assume that $A$ has full column rank.

**Result:** If $\mathbf{u}_{1},\dots, \mathbf{u}_{k}$ are pairwise orthogonal vectors, then they are linearly independent.

Suppose that the columns of $A$ are orthogonal, i.e., 
$$(\mathbf{a}^{(i)})^T\mathbf{a}^{(j)}=0 \text{ for all }i \neq j.$$
Suppose $(\theta_{1},\dots,\theta_{d})$ is a solution:
$$
\begin{align}
\theta_{1}\mathbf{a}^{(1)} + \dots + \theta_{d}\mathbf{a}^{(d)}&=\mathbf{b} \\
\implies \theta_{j}(\mathbf{a}^{(j)})^T\mathbf{a}^{(j)} &= (\mathbf{a}^{(j)})^T\mathbf{b}; \forall j\in \{ 1,\dots,d \} \\
\implies \theta_{j} &= \frac{(\mathbf{a}^{(j)})^T\mathbf{b}}{(\mathbf{a}^{(j)})^T\mathbf{a}^{(j)}}; \forall j \in \{ 1,\dots,d \}.
\end{align}$$
Note that
$$\begin{align}
A^TA &= \begin{pmatrix}
(\mathbf{a}^{(1)})^T \\
\vdots \\
(\mathbf{a}^{(d)})^T
\end{pmatrix}
\begin{pmatrix}
\mathbf{a}^{(1)} & \dots & \mathbf{a}^{(d)}
\end{pmatrix} \\
&= \text{diag}((\mathbf{a}^{(1)})^T\mathbf{a}^{(1)},\dots,(\mathbf{a}^{(d)})^T\mathbf{a}^{(d)}).
\end{align}$$
Thus, 
$$(A^TA)^{-1}= \text{diag}\left( \frac{1}{(\mathbf{a}^{(1)})^T\mathbf{a}^{(1)}},\dots, \frac{1}{(\mathbf{a}^{(d)})^T\mathbf{a}^{(d)} }\right).$$
Observe that
$$\begin{align}
\tilde{\theta} &= \begin{pmatrix}
\frac{(\mathbf{a}^{(1)})^T\mathbf{b}}{(\mathbf{a}^{(1)})^T\mathbf{a}^{(1)}} \\
\vdots \\
\frac{(\mathbf{a}^{(d)})^T\mathbf{b}}{(\mathbf{a}^{(d)})^T\mathbf{a}^{(d)}}
\end{pmatrix} \\ 
&= \begin{pmatrix}
\frac{(\mathbf{a}^{(1)})^T}{(\mathbf{a}^{(1)})^T\mathbf{a}^{(1)}} \\
\vdots \\
\frac{(\mathbf{a}^{(d)})^T}{(\mathbf{a}^{(d)})^T\mathbf{a}^{(d)}}
\end{pmatrix}\begin{pmatrix}
b_{1} \\
\vdots \\
b_{n}
\end{pmatrix}\\ 
&= \begin{pmatrix}
\frac{1}{(\mathbf{a}^{(1)})^T\mathbf{a}^{(1)}} & \dots & 0 \\
\vdots & \ddots & \vdots \\
0 & \dots & \frac{1}{(\mathbf{a}^{(d)})^T\mathbf{a}^{(d)}}
\end{pmatrix}\begin{pmatrix}
(\mathbf{a}^{(1)})^T \\
\vdots\\
(\mathbf{a}^{(d)})^T
\end{pmatrix}\begin{pmatrix}
b_{1} \\
\vdots \\
b_{n}
\end{pmatrix}\\
&= \text{diag}\left( \frac{1}{(\mathbf{a}^{(1)})^T\mathbf{a}^{(1)}},\dots, \frac{1}{(\mathbf{a}^{(d)})^T\mathbf{a}^{(d)} }\right)\begin{pmatrix}
(\mathbf{a}^{(1)})^T \\
\vdots\\
(\mathbf{a}^{(d)})^T
\end{pmatrix}\mathbf{b} \\
&= (A^TA)^{-1}A^T\mathbf{b}.
\end{align}$$