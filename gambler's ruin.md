---
tags:
  - info
  - college
  - stochastic_processes
---
# Setup
Consider two gamblers $A$ and $B$ with initial capital $a$ and $b$ respectively. Each time a fair coin is tossed. If $H$ turns up, then $A$ gets 1 rupee from $B$, otherwise $B$ gets 1 rupee from $A$.

The total capital is given by
$$N=a+b.$$
The capital of $A$ after $n$ tosses is given by
$$S_{n} = \begin{cases}
a; \text{ if }n=0 \\
a+\sum_{i=1}^n \epsilon_{i}; \text{ if }n\geq 1.
\end{cases}$$
Denote the number of tosses $A$ takes to reach capital $i$ by $T_{i}$.

We are interested in
$$\mathbb{P}(S_{n}=N \text{ for some }n\geq 1\text{ before }S_{n}=0\text{ for some }n\geq 1)=\mathbb{P}(T_{N}<T_{0}).$$
# Solution


Equation 1: For $n \geq 1$, we have
$$\begin{align}
u_{2n} &= \mathbb{P}(S_{2n}=0) \\
&= \mathbb{P}(S_{2n}=0; S_{k} \neq 0 \text{ for all }k=1,\dots,2n-1) \\
&+\mathbb{P}(S_{2n}=0; S_{2k}=0 \text{ for some }k=1,\dots,n-1).
\end{align}$$
The second term can be written as
$$\begin{align}
\mathbb{P}(S_{2n}=0; S_{2k}=0 \text{ for some }k=1,\dots,n-1)&= \sum_{i=1}^{n-1}\mathbb{P}(B_{2i} \cap \{ S_{2n}=0 \}).
\end{align}$$
Note that
$$\begin{align}
\mathbb{P}(B_{2i} \cap \{ S_{2n}=0 \})&=\mathbb{P}(S_{1} \neq 0 ;\dots;S_{2i-1}\neq 0; S_{2i}=0; S_{2n}=0) \\
&= \mathbb{P}(\underbrace{S_{1} \neq 0; \dots; S_{2i-1} \neq 0;S_{2i}=0 }_{\text{depends on }(\epsilon_{1},\dots,\epsilon_{2i})};\underbrace{S_{2n}-S_{2i}=0}_{\text{depends on }(\epsilon_{2i+1},\dots,\epsilon_{2n})}) \\
&= \mathbb{P}(S_{1} \neq 0; \dots;S_{2i-1} \neq 0; S_{2i} =0)\cdot \mathbb{P}(S_{2n}-S_{2i}=0) \\
&= f_{2i}\cdot u_{2n-2i}.
\end{align}
$$
The last step is true because:
$$S_{2n}-S_{2i}=\sum_{k=2i+1}^{2n}\epsilon_{i} \overset{d}{=} \sum_{k=1}^{2n-2i}\epsilon_{i}=S_{2n-2i}.$$
Plug this in equation 1. For $n\geq 1$, we get
$$\begin{align}
u_{2n} &= f_{2n} + \sum_{i=1}^{n-1}f_{2i}\cdot u_{2n-2i} \\
&= f_{2n}\cdot u_{0} + \sum_{i=1}^{n-1}f_{2i}\cdot u_{2n-2i} + u_{2n}f_{0} \\
&= \sum_{i=0}^n f_{2i}\cdot u_{2n-2i}.
\end{align}$$
Note that $\{ u_{2n} \}$ is a convolution for $\{ f_{2n} \}$ and $\{ u_{2n} \}$ except for $n=0$ (since $1=u_{0} \neq f_{0}u_{0}=0\cdot 1=0$).