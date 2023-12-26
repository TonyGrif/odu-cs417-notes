---
tags:
  - Approximation
---
# $X^TX$ | $X^TY$ Method
This simple method of [[Least-Squares Approximation Overview | least-squares approximation]] involves translating a set of points to matrix form and utilizing row matrix operations to approximate a function. The exponent of the function depends on the given [[Least-Squares Approximation Overview#Basis Functions | basis functions]].
## Example
Given the following table, calculate $\hat{\varphi}(x)=c_0+c_1x$

| x-point | y-point |
|---      | ---     |
| -2 | 4 |
| -1 | 1 |
| 0 | 0 |

$$ 
[X]= 
\begin{bmatrix}
1 & -2 \\
1 & 1 \\
1 & 0 \\
\end{bmatrix}
$$
$$
[X^T]=
\begin{bmatrix}
1 & 1 & 1 \\
-2 & 1 & 0
\end{bmatrix}
$$
$$
[Y]=
\begin{bmatrix}
4 \\
1 \\
0 
\end{bmatrix}
$$
$$
[X^TX]=
\begin{bmatrix}
3 & -3 \\
-3 & 5
\end{bmatrix}
$$
$$
[X^TY]=
\begin{bmatrix}
5 \\
9
\end{bmatrix}
$$
$$
[X^TX]|[X^TY]=
\begin{bmatrix}
3 & -3 & c_0 & | & 5\\
-3 & 5 & c_1 & | & 9
\end{bmatrix}
$$
Using row matrix operations leads to $c_0=\dfrac{-1}{3}$ and $c_1=-2$. Thus, $\hat{\varphi}(x)=\dfrac{-1}{3}-2x$.