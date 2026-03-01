---
tags:
  - problem
  - college
  - linear_statistical_models
---
# Problem
We study the effect of $\epsilon$ on the regression estimates. We consider the simple linear regression setup. We begin by fixing the values of $\alpha$ and $\beta$. We also generate $100$ observations from $\mathcal{N}(5,1)$ and designate them as $x_{1},\dots,x_{100}$.

## Part a

Fix $\sigma^2 =1$. Construct $y$ using $y_{i} = \alpha+\beta x_{i} + \epsilon_{i}$ for $i = 1,\dots,100$, where $\epsilon_{i} \overset{\text{iid}}{\sim} \mathcal{N}(0, \sigma^2)$.
# Solution
## Part a and Part b

```r
x <- rnorm(n = 100,mean = 5, sd = 1)
generate_data <- function(sigma_square){
	y = 2 + 3 * x + rnorm(n = 100, mean = 0, sd = sqrt(sigma_square))
	model <- lm(y ~ x)
	return(coef(model))
}
```

## Part c

```r
results_
```