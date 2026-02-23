---
tags:
  - info
  - college
  - statistical_methods
  - non_parametric
---
# Setup
Suppose $X_{1},\dots,X_{n_{1}} \overset{\text{iid}}{\sim}F_{1}$ and $Y_{1},\dots,Y_{n_{2}} \overset{\text{iid}}{\sim}F_{2}$.

We want to test if they are of the same "scale".

Assumptions:
1. The two samples are independent of each other. 
2. $F_{1}$ and $F_{2}$ must be continuous.
3. $F_{1}$ and $F_{2}$ must have the same form; and may differ only by location/scale under the null.
# Procedure
1. Estimate their "centers" $\mu_{X}$ and $\mu_{Y}$ by their sample medians $\hat{\mu}_{X}$ and $\hat{\mu}_{Y}$.
2. Define $\{ U_{i} \}_{i=1}^{n_{1}}$ by $U_{i}:=|X_{i} - \hat{\mu}_{X}|$ and $\{ V_{i} \}_{i=1}^{n_{2}}$ by $V_{i} := |Y_{i} - \hat{\mu}_{Y}|$. If their scale significantly differs, we expect one of them to be "generally larger" than the other.
3. Peform [[wilcoxon's rank sum test]] on $\{ U_{i} \}$ and $\{ V_{i} \}$.