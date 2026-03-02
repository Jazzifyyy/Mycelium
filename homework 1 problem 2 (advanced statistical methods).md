---
tags:
  - problem
  - statistical_methods
  - college
---
```r
set.seed(123)

reject_t <- numeric(1000)
reject_wilcox <- numeric(1000)
reject_t_new <- numeric(1000)
reject_wilcox_new <- numeric(1000)

for (i in 1:1000) {
  t <- rt(30, 2)
  
  p_value_t <- t.test(t, mu = 0)$p.value
  reject_t[i] <- p_value_t < 0.05
  
  p_value_wilcox <- wilcox.test(t, mu = 0)$p.value
  reject_wilcox[i] <- p_value_wilcox < 0.05
  
  t_new <- rt(30, 2) + 0.5
  
  p_value_t_new <- t.test(t_new, mu = 0)$p.value
  reject_t_new[i] <- p_value_t_new < 0.05
  
  p_value_wilcox_new <- wilcox.test(t_new, mu = 0)$p.value
  reject_wilcox_new[i] <- p_value_wilcox_new < 0.05
}

results <- data.frame(
  Test = c("t-test", "Wilcoxon"),
  Empirical_Size = c(mean(reject_t), mean(reject_wilcox)),
  Empirical_Power = c(mean(reject_t_new), mean(reject_wilcox_new))
)

print(results)

```


```
      Test Empirical_Size Empirical_Power
1   t-test          0.042            0.29
2 Wilcoxon          0.050            0.47
```
Note that the Wilcoxon's test has more power compared to the t-test.