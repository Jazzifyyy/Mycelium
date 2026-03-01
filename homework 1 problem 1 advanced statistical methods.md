---
tags:
  - problem
  - statistical_methods
  - college
---
# Problem
This dataset is drawn from a study discussed by Siegel (1956). It involves eight pairs of identical twins who are of nursery school age. In the study, for each pair, one is randomly selected to attend nursery school while the other remains at home. At the end of the study period, all 16 children are given the same social awareness test. The scores are given below. Conduct an appropriate test of the hypothesis that the median of the distribution of difference of scores between school and home trained twins is positive.


| school | home |
| ------ | ---- |
| 82     | 63   |
| 69     | 42   |
| 73     | 74   |
| 43     | 37   |
| 58     | 51   |
| 56     | 43   |
| 76     | 80   |
| 65     | 62   |
# Solution
We use [[wilcoxon's signed rank test]] where $X_{i}$'s are obtained after subtracting the home score from the school score of the $i$th pair.

| school | home | $X_{i}$ = school - home | $Y_{i} = \mathbb{1}(X_{i} > 0)$ | \|$X_{i}$\| | $R_{i}$ | $R_{i}Y_{i}$ |
| ------ | ---- | ----------------------- | ------------------------------- | ----------- | ------- | ------------ |
| 82     | 63   | 19                      | 1                               | 19          | 7       | 7            |
| 69     | 42   | 27                      | 1                               | 27          | 8       | 8            |
| 73     | 74   | -1                      | 0                               | 1           | 1       | 0            |
| 43     | 37   | 6                       | 1                               | 6           | 4       | 4            |
| 58     | 51   | 7                       | 1                               | 7           | 5       | 5            |
| 56     | 43   | 13                      | 1                               | 13          | 6       | 6            |
| 76     | 80   | -4                      | 0                               | 4           | 3       | 0            |
| 65     | 62   | 3                       | 1                               | 3           | 2       | 2            |
The test statistic is $T = \sum_{i=1}^8 R_{i}Y_{i}=32$.

Note that for $Y \in \{ 1,2,3,4,5 \}$, we don't have favourable outcomes. 

If $Y = 6$, we have $(2,4,5,6,7,8)$ and $()$