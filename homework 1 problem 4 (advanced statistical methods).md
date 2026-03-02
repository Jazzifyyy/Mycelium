---
tags:
  - problem
  - statistical_methods
  - college
---
We perform the Kruskal-Wallis to test if the location of the distributions of the unoccupied beds in the three hospitals are different.

```r
hosp1 <- c(6, 38, 3, 17, 11, 30, 15, 16, 25, 5)
hosp2 <- c(34, 28, 42, 13, 40, 31, 9, 32, 39, 27)
hosp3 <- c(13, 35, 19, 4, 29, 0, 7, 33, 18, 24)

beds_list <- list(hosp1, hosp2, hosp3) 

kruskal.test(beds_list)
```

Output:
```
	Kruskal-Wallis rank sum test

data:  beds_list
Kruskal-Wallis chi-squared = 6.0988, df = 2, p-value = 0.04739
```
Thus, we reject the null that the number of unoccupied beds are the same for the three hospitals since the p value is less than $0.05$.