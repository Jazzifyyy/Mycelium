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
We use [[wilcoxon's rank sum test]]. Let the scores of individuals that attended school to be $X_{i}$'s and the other case be $Y_{i}$'s.

The pooled sample is: $(37, 42, 43, 43, 51, 56, 58, 62, 63, 65, 69, 73, 74, 76, 80, 82)$ and the adjusted rankings are $(1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16)$. Ajusted ranks for ties are $(1,2,3.5, 3.5,5,6,7,8,9,10,11,12,13,14,15,16)$.

Sum of ranks that came from $X$ is $$
