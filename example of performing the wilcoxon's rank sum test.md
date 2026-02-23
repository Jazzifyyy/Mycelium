---
tags:
  - college
  - statistical_methods
  - info
  - non_parametric
---
To perform [[wilcoxon's rank sum test]].

# R function
Example:
```r
wilcox.test( c(0.80, 0.83, 1.89, 1.04, 1.45, 1.38, 1.91, 1.64, 0.73, 1.46), c(1.15, 0.88, 0.90, 0.74, 1.21),alternative="greater")
```
Output:
```r
Wilcoxon rank sum exact test

data:  c(0.8, 0.83, 1.89, 1.04, 1.45, 1.38, 1.91, 1.64, 0.73, 1.46) and c(1.15, 0.88, 0.9, 0.74, 1.21)
W = 35, p-value = 0.1272
alternative hypothesis: true location shift is greater than 0
```

# Manually

```r
x <- c(0.80, 0.83, 1.89, 1.04, 1.45, 1.38, 1.91, 1.64, 0.73, 1.46)
y <- c(1.15, 0.88, 0.90, 0.74, 1.21)
z<-sort(c(x,y))
T<-sum(which(z %in% x))-10*11/2
T

# n denotes the total length, m denotes the length of x

ranksum<-function(n,m,T){
T=T+m*(m+1)/2
x<-c(1:n)
l<-choose(n,m)
k<-rep(0,l)
y<-combn(x,m)
for(j in 1:l){
k[j]<-sum(x[y[,j]])}
  pval<-length(which(k>=T))/choose(n,m)
return(pval)
}
ranksum(15,10,35)
```