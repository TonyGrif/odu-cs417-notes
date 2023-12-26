---
tags:
  - Interpolation
---
# Newton's Form
$$P_n(x) = \sum_{i=0}^{n}(f[x_0,x_1,...,x_i]\prod_{k=0}^{i-1}(x-x_k))$$
Where $f[x_0,x_1,...,x_i]=\dfrac{f[x_1,x_2,...x_k]-f[x_0,x_1,...x_{k-1}]}{x_k-x_0}$ ([[Newton's Form#^24bfe2 | property two]])
## Divided Difference
$f[x_0,x_1,...x_i]$ is the divided difference between a collection of points. For a pair of points, it is calculated as $f[x_i,x_j]=\dfrac{f_i-f_j}{x_i-x_j}$. $f[x_0]$ always equals $f(x_0)$. For a sequence of points, it is calculated as $f[x_0,x_1,...x_n]=\dfrac{f[x_0-x_1]-...-f[x_{n-1}-x_n]}{x_n-x_0}$.
## Properties
1. Iterative Form: $f[x_0,x_1,...,x_n]=\sum_{i=0}^{n}(\dfrac{f_i}{\prod_{j=0 \ j\ne i}^{n}(x_i-x_j)})$
2. Recursive Form: $f[x_0,x_1,...,x_n]=\dfrac{f[x_1,x_2,...x_k]-f[x_0,x_1,...x_{k-1}]}{x_k-x_0}$ ^24bfe2
3. Symmetry: $f[x_0, x_1, x_2,...,x_k]=f[x_k, x_2, ...x_0, x_1]$ (order doesn't matter)
## Example
Given the following points, calculate:

| x-points | y-points |
| ---- | ---- |
| -1 | 1 | 
| 0 | 0 | 
| 1 | 1 |

$$
f[x_0, x_1] = \dfrac{-1-0}{1-0}=-1; f[x_1,x_2]=\dfrac{1-0}{1-0}=1
$$
$$
f[x_0, x_1, x_2]=\dfrac{f[x_0, x_1]-f[x_1,x_2]}{x_2-x_0}=\dfrac{-1-1}{-1-1}=1
$$
$$
P_2(x)=f[x_0]+f[x_0,x_1](x-x_0)+f[x_0,x_1,x_2](x-x_0)(x-x_1)=
$$
$$
P_2(x)=1+(-1)(x+1)+1(x+1)(x-0)=1-x-1+x^2+x=x^2
$$