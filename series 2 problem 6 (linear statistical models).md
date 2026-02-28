---
tags:
  - problem
  - linear_statistical_models
  - college
---
# Problem
We study the *consistency* property of the least squares estimators in simple linear regression setup.

## Part a
Fix the sample size $n = 25$. Also fix two constants $\alpha$ and $\beta$. Generate $x_{1},\dots,x_{n} \overset{\text{iid}}{\sim} \mathcal{N}(25,4)$. Treat these as fixed covariates.

## Part b
Construct $y_{1},\dots,y_{n}$ using $y_{i}=\alpha+\beta x_{i}+\epsilon_{i}$ for $i = 1,\dots,n$, where $\epsilon_{i} \overset{\text{iid}}{\sim} \mathcal{N}(0,1)$. Fit a simple linear regression model to find the estimates of $\alpha$ and $\beta$.
# Solution

## Part a
```r {pre}
n <- 25
alpha <- 2
beta <- 3
x <- rnorm(n, mean = 25, sd = 2)
print(x)
```
## Part b

```r
epsilon <- rnorm(n, mean = 0, sd = 1)
y <- alpha + beta * x + epsilon
model <- lm(y ~ x)
model
```