---
tags:
  - college
  - info
  - statistical_methods
---
# Setup and assumptions

Suppose $X_{1},\dots,X_{n} \overset{\text{iid}}{\sim}f$ where $\text{median}(X_{i}) = \theta$. 

Assumptions: 
1. $f$ is a continuous distribution. 
2. $f$ is a symmetric distribution.

# Motivation

Under the null hypothesis, we expect our observations to surround the true median "in an equal manner" (this is quantified by the test statistic below). If the observations seems to be deviating towards one side, then we have more reason to believe that the null hypothesis is false.

Note that if $f$ is not symmetric, then the observations might trail towards one side, which might result in incorrect conclusions. 
# Test procedure

Assume for simplicity that the observations in the sample have distinct values and that no observation equals the median.

1. Compute $|X_{1} - \theta_{0}|,\dots,|X_{n}- \theta_{0}|$.
2. Sort these values and use the sorted list to assign ranks $R_{1},\dots,R_{n}$ such that the rank of the smallest observation is one, the rank of the next smallest is two, and so on.
3. Define $$Y_{i} = \begin{cases}
1; \text{ if }X_{i}> \theta_{0} \\
0; \text{ otherwise}.
\end{cases}$$
4. The test statistic is defined as
   $$T = \sum_{i=1}^n R_{i}Y_{i}.$$
5. Compute the appropriate p-value for the test by using the distribution of $T$.
# Distribution of the test statistic

We ask the question: How many ways can we have a set of ranks that add up to a specified number. We then divide that number by the total number of ranks that our observations can possibly yield. That ratio is $\mathbb{P}(T=t)$.

The following passage introduces some notation that enables us to conveniently determine this ratio.

Define 
$$Y := \sum_{i=1}^n Y_{i}$$
which denotes the number of observations that exceeds the hypothesized median.

Note that the test statistic is of the form
$$T = \sum_{i=1}^Y r_{i}$$
where $1\leq r_{1}<\dots<r_{Y}\leq n$ (note the strictness of the equality and the simplicity assumption done at the beginning) and $r_{i}$'s are the ranks corresponding to only those values that exceed the hypothesized mean. (Thus, the elements of $(r_{1},\dots,r_{Y})$ is "cherry picked" from $(R_{1},\dots,R_{n})$.)

Notice that there are $2^n$ values that the vector $\mathbf{Y}=(Y_{1},\dots,Y_{n})$ can take with equal probability: $\frac{1}{2^n}$.

Each values of $\mathbf{Y}$ correspond to exactly one $\mathbf{r} = (r_{1},\dots,r_{Y})$, and thus, there are $2^n$ values that the vector $\mathbf{r}$ can take with equal probabilities.

We can then use elementary counting techniques to get $\mathbb{P}(T=t)$ for all values of $t$ to get the required distribution.

## Example

Suppose we have $7$ observations and we want to find $\mathbb{P}(T = 9)$, thus $n=7$ and $t=9$.

Recall that $Y$ denotes the number of observations that exceeds the hypothesized median.

+ If $Y=1$, then there is no vector consisting of one element from $1$ to $7$ that can sum to $9$.
+ If $Y=2$, we have $(2,7), (3,6),(4,5)$.
+ If $Y=3$, we have $(1,2,6), (1,3,5), (2,3,4)$.
+ If $Y\geq4$, we do not have any more vectors since ties are not allowed.

Then, $\mathbb{P}(T=9) = \frac{6}{2^7}$.

# Also See:
+ [[example of performing the wilcoxon's signed rank test]]