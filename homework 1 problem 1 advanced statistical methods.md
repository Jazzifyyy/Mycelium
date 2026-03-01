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
We use [[wilcoxon's signed rank test]] where $X_{i}$'s are obtained after subtracting the home score from the school score of the $i$th pair. We get $()$