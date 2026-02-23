---
tags:
  - info
  - college
  - linear_statistical_models
---
# Problem 

Suppose that we have data on the salary of employees in a company and their educational qualification is shown in the table below. 

We want to see if (and how) the salary of an employee depenhds on his/her educational qualification. For this, we consider the following model for the salary $(y)$:
$$y = \theta_{0}+\theta_{1}x_{1}+\theta_{2}x_{2}+\theta_{3}x_{3}+\epsilon$$
and $\mathbb{E}[\epsilon]=0$.

Table:

| Employee Id | Salary | Highest education  |
| ----------- | ------ | ------------------ |
| 1201        | 50000  | BSc in Mathematics |
| 1005        | 35000  | Class XII          |
| 1001        | 80000  | B. Com             |
| 1135        | 90000  | MSc                |
| 1093        | 95000  | MBA                |
| 1013        | 25000  | Class VIII         |
| 1257        | 30000  | Class XII          |
| 1178        | 20000  | Class VIII         |
In the model, $x_{1}$ is the indicator of completing high school education (i.e., $x_{1}=1$ if the employee has completed high school (class XII); otherwise $x_{1}=0$), $x_{2}$ is the indicator of completing college education (bachelor's degree) and $x_{3}$ is the indicator of completing university education (master's degree).

1. Write the model in the vector-matrix notation $\mathbf{y}=X \tilde{\theta}+\epsilon$. Write down the response vector $\mathbf{y}$ and the data matrix $X$ based on the observations in the table.
2. What do the parameters $\theta_{0}, \theta_{1},\theta_{2}, \theta_{3}$ signify?
3. Based on the model, how can you formulate the question: "does salary depend on the level of education?"
Now consider a different model for the same data:
$$y = \gamma_{1}x_{1}+\gamma_{2}x_{2}+\gamma_{3}x_{3}+\epsilon.$$
4. Write the new model in vector-matrix notation $\mathbf{y}=X'\tilde{\gamma} + \epsilon.$
5. Is there any connection between the two models?

# Solution

## Part a

The model in vector-matrix notation is 
$$\begin{pmatrix}
y_{1} \\
\vdots \\
y_{n}
\end{pmatrix} = \begin{pmatrix}
1 & x_{11} & x_{21} & x_{31} \\
\vdots & \vdots & \vdots & \vdots \\
1 & x_{1n} & x_{2n} & x_{3n}
\end{pmatrix}
\begin{pmatrix}
\theta_{0} \\
\theta_{1} \\
\theta_{2} \\
\theta_{3}
\end{pmatrix} + \begin{pmatrix}
\epsilon_{1} \\
\vdots \\
\epsilon_{n}
\end{pmatrix}$$

The response vector is given by $\mathbf{y}=(50000, 35000, 80000, 90000, 95000, 25000, 30000, 20000)^T$ and the data matrix is given by
$$X = \begin{pmatrix}
1 & 1 & 1 & 0 \\
1 & 1 & 0 & 0 \\
1 & 1 & 1 & 0 \\
1 & 1 & 1& 1 \\
1 & 1 & 1 & 1 \\
1 & 0 & 0 & 0 \\
1 & 1 & 0 & 0 \\
1 & 0 & 0 & 0
\end{pmatrix}$$
## Part b

Note that we have $\mathbb{E}[y | x_{1}=0; x_{2}=0; x_{3}=0]= \theta_{0}$, $\mathbb{E}[y | x_{1}=1, x_{2}=0, x_{3}=0]=\theta_{0}+\theta_{1}$, $\mathbb{E}[y|x_{1}=1, x_{2}=1, x_{3}=0]=\theta_{0}+\theta_{1}+\theta_{2}$, $\mathbb{E}[y|x_{1}=1, x_{2}=1, x_{3}=1]=\theta_{0}+\theta_{1}+\theta_{2}+\theta_{3}$. 

 + $\theta_{0}$ denotes the average salary for individuals that have not completed high school education.
 + $\theta_{1}$ denotes the increase in average salary upon completing high school education.
 + $\theta_{2}$ denotes the increase in average salary upon completing college education.
 + $\theta_{3}$ denotes the increase in average salary upon completing university education.
## Part c

Salary does not depend on education iff changing education level does not change the conditional mean of $y$.

The question is formulated by the following null and alternative hypotheses:
$$H_{0}: \theta_{1}=\theta_{2}=\theta_{3}=0 \text{ v.s. }H_{a}: \text{ atleast one of }\theta_{1},\theta_{2},\theta_{3},\theta_{4} \neq 0$$
## Part d

$$\begin{pmatrix}
y_{1} \\
\vdots \\
y_{n}
\end{pmatrix} = \begin{pmatrix}
x_{11} & x_{21} & x_{31} \\
\vdots & \vdots & \vdots \\
x_{1n} & x_{2n} & x_{3n}
\end{pmatrix}
\begin{pmatrix}
\gamma_{1} \\
\gamma_{2} \\
\gamma_{3}
\end{pmatrix} + \begin{pmatrix}
\epsilon_{1} \\
\vdots \\
\epsilon_{n}
\end{pmatrix}$$


The data matrix $X'$ is given by
$$X'=\begin{pmatrix}
1 & 1 & 0 \\
1 & 0 & 0 \\
1 & 1 & 0 \\
1 & 1& 1 \\
1 & 1 & 1 \\
0 & 0 & 0 \\
1 & 0 & 0 \\
0 & 0 & 0
\end{pmatrix}$$
## Part e
+ $\gamma_{1}$ denotes the average salary for individuals that have completed high school education.
 + $\gamma_{2}$ denotes the increase in average salary upon completing college education.
 + $\gamma_{3}$ denotes the increase in average salary upon completing university education.
## Part f

Model 2 is Model 1 with the intercept constrained to zero. By removing the intercept, Model 2 assumes that without a high school education, the mean salary is zero.

## Part g

In vector-matrix notation, Model 3 can be written as:

$$\begin{pmatrix}
y_{1} \\
\vdots \\
y_{n}
\end{pmatrix} = \begin{pmatrix}
1 & x_{11} & x_{21} \\
\vdots & \vdots & \vdots \\
1 & x_{1n} & x_{2n} 
\end{pmatrix}
\begin{pmatrix}
\delta_{0} \\
\delta_{1} \\
\delta_{2} \\
\end{pmatrix} + \begin{pmatrix}
\epsilon_{1} \\
\vdots \\
\epsilon_{n}
\end{pmatrix}$$

The data matrix for Model 3 is given by
$$X'' = \begin{pmatrix}
1 & 1 & 1\\
1 & 1 & 0\\
1 & 1 & 1\\
1 & 1 & 1\\
1 & 1 & 1\\
1 & 0 & 0\\
1 & 1 & 0 \\
1 & 0 & 0 
\end{pmatrix}$$

+ $\delta_{0}$ denotes the average salary for individuals that do not have a high school education.
+ $\delta_{1}$ denotes the increase in average salary upon completing high school education.
+ $\delta_{2}$ denotes the increase in average salary upon completing college education.

Model 3 is Model 1 with the assumption that there is zero increase in average salary upon completing university education. 

In vector-matrix notation, Model 4 can be written as

$$\begin{pmatrix}
y_{1} \\
\vdots \\
y_{n}
\end{pmatrix} = \begin{pmatrix}
1 & x_{21} & x_{31} \\
\vdots & \vdots & \vdots \\
1 & x_{2n} & x_{3n} 
\end{pmatrix}
\begin{pmatrix}
\tau_{0} \\
\tau_{2} \\
\tau_{3} \\
\end{pmatrix} + \begin{pmatrix}
\epsilon_{1} \\
\vdots \\
\epsilon_{n}
\end{pmatrix}$$

The data matrix for Model 4 is given by
$$X''' = \begin{pmatrix}
1 & 1 & 0 \\
1 & 0 & 0 \\
1 & 1 & 0 \\
1 & 1& 1 \\
1 & 1 & 1 \\
1 & 0 & 0 \\
1 & 0 & 0 \\
1 & 0 & 0
\end{pmatrix}.$$
+ $\tau_{0}$ denotes the average salary for individuals that do not have a high school education.
+ $\tau_{2}$ denotes the increase in average salary upon completing college education.
+ $\tau_{3}$ denotes the increase in average salary upon completing university education.

Model 4 is Model 1 with the assumption that there is zero increase in average salary upon completing high school education. 