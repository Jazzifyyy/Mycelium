---
tags:
  - college
  - info
  - statistical_methods
  - R
---
To perform [[wilcoxon's signed rank test]].
# R function

Example

```r
library(stats)
a<-c(73, 82, 87, 68, 106, 60,97)
wilcox.test(a, mu = 70, alternative = "greater")
```
Output:
```r
Wilcoxon signed rank exact test

data:  a
V = 24, p-value = 0.05469
alternative hypothesis: true location is greater than 70
```

# Manually

First note the following function:
```r
#This generates all possible subsets of size 2 when $n=4$.
combn(c(1:4),2)
```
Output:
```r
     [,1] [,2] [,3] [,4] [,5] [,6]
[1,]    1    1    1    2    2    3
[2,]    2    3    4    3    4    4
```

```r
#Writing own function for p-value of signed rank test
signrank<-function(n,T){
  x<-c(1:n)
  k<-0
  for(i in 1:n){
    y<-combn(x,i)
    l<-dim(y)[2]
    for(j in 1:l){
      k<-cbind(k,sum(x[y[,j]]))}
  }
  pval<-length(which(k>=T))/length(k)
  return(pval)
}
table(k)
#Signed rank test for the example done in class
a<-c(73, 82, 87, 68, 106, 60,97)
b<-a-70
r<-rank(abs(b))
s<-ifelse(b>0,1,0)
T<-sum(r*s)
signrank(7,T)
```