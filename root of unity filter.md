# Statement
Suppose we have a polynomial $F(x) = a_{0}+a_{1}x+a_{2}x^2+\dots$. Then the sum of coefficients of $F$ such that the corresponding power of $x$ is a multiple of a number $n$ is given by
$$a_{0}+a_{n}+a_{2n}+\dots = \frac{1}{n}(F(1)+F(w)+\dots +F(w^{n-1}))$$
where $w = e^{2\pi i /n}$.

# Proof
Let $s_{k} = 1+w^k + w^{2k}+\dots+ w^{(n-1)k}$.

Note that if $n$ divides $k$, then $w^k=1$ and so $s_{k}=1+\dots+1= n$. Otherwise, 
$$s_{k}= \frac{1-w^{nk}}{1-w^k}=0.$$
(...)

https://math.stackexchange.com/questions/3213142/root-of-unity-filter