---
tags:
  - Interpolation
---
# Lagrange Form
$$ P_n(x) = \sum_{i=0}^{n} f_il_i(x) $$
Where $f_i = f(x_i)$ and $l_i = \prod\limits_{k=0 \; k\ne i}^{n} \dfrac{x-x_k}{x_i-x_k}$ and $n$ is the number of points we have minus 1.
## Properties
1) If $l_i$ is a polynomial of degree $n$, $P_n(x)$ is also of degree $n$
2) $l_i(x)$ satisfies $l_i(x_k) = \delta_{ik}$ if $\delta_{ik} = 1$ when $i=k$ ($\delta_{ik}=0$ otherwise) and $\sum_{i=0}^{n} l_i(x) = 1$ 
3) $P_n(x_i) = \sum_{i=0}^{n} f_i l_i(x) = f(x_i)$ 
## Example
Given the following points, solve:

| x-points | y-points|
| --- | --- |
| -1 | 1 |
| 0 | 0 |
|1 | 1 | 

$$
\def\s{\sum_{i=0}^2}
P_2(x)= \s f_i l_i(x) = f_0l_0 + f_2l_2= 1(l_0)+1(l_2) = l_0+l_2
$$
$$
\prod_{k=0; k\ne0}^2\dfrac{x-x_k}{x_0-x_k} + \prod_{k=0; k\ne2}^2\dfrac{x-x_k}{x_2-x_k}
$$
$$
\dfrac{x-0}{-1-0}\times\dfrac{x-1}{-1-1} + \dfrac{x-(-1)}{1-(-1)}\times\dfrac{x-0}{1-0}
$$
$$
\dfrac{x}{-1}\times\dfrac{x-1}{-2} + \dfrac{x+1}{2}\times\dfrac{x}{1}=
\dfrac{x(x-1)}{2}+\dfrac{x(x+1)}{2}=x^2
$$
