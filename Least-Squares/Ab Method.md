---
tags:
  - Approximation
---
# $A\vec{b}$ Method
This robust method of [[Least-Squares Approximation Overview | least-squares approximation]] utilizes summation/integrals to calculate an approximation function for a given basis function. This method skips the redundant matrix set up of the $X^TX|X^TY$ [[XTX & XTY Method | method]].
## Equation
For given basis functions $\pi_0$ and $\pi_1$ ...
$$
\def\rsum{\sum_{k=1}^{n}}
\def\xsub{x_k}
\begin{bmatrix}
\rsum \pi_0(\xsub)\pi_0(\xsub) & \rsum \pi_0(\xsub)\pi_1(\xsub) & | & \rsum \pi_0(\xsub) f(\xsub) \\
\rsum \pi_1(\xsub)\pi_0(\xsub) & \rsum\pi_1(\xsub)\pi_1(\xsub) & | & \rsum \pi_1(\xsub)f(\xsub)
\end{bmatrix}
$$
## Example
Given the following points calculate the assigned case, let $f(x)=2x^3$ and $\varphi = c_0 + c_1x$. 

| x-point | y-point | 
| --- | --- |
| $-\alpha$ | $-\alpha^3$ |
| 0 | 0 |
| $\alpha$ | $\alpha^3$ |
Based on $\varphi$, we can say $\pi_0(x) = 1$ and $\pi_1(x) = x$.
### Discrete Case
$$
\def\sm{\sum_{i=0}^2}
\begin{bmatrix}
\sm 1 & \sm x_i & | & \sm 2(x_i)^3 \\
\sm x_i & \sm (x_i)^2 & | & \sm 2(x_i)^4
\end{bmatrix}
$$
$$
\begin{bmatrix}
3 & -\alpha+0+\alpha & | & 2(-\alpha)^3 + 0 + 2(\alpha)^3 \\
-\alpha+0+\alpha & (-\alpha)^2+0+\alpha^2 & | & 2(-\alpha)^4+0+2(\alpha)^4
\end{bmatrix}
$$
$$
\begin{bmatrix}
3 & 0 & | & 0 \\
0 & 2\alpha^2 & | & 4\alpha^4
\end{bmatrix}
$$
Using row matrix operations, $\pi_1=2\alpha^2$.
Thus, $\hat\varphi=2\alpha^2x$.
### Continuous Case
$$
\def\in{\int_{-\alpha}^{\alpha}}
\begin{bmatrix}
\in 1 d x & \in x d x & | & \in 2(x)^3 \\
\in x d x & \in x^2 d x & | & \in 2(x)^4
\end{bmatrix}
$$
$$
\def\loi{|_{-\alpha}^{\alpha}}
\begin{bmatrix}
x \loi & \dfrac{1}{2}x^2 \loi & | & \dfrac{2}{4}x^4 \loi \\
\dfrac{1}{2}x^2 \loi & \dfrac{1}{3}x^3 \loi & | & \dfrac{2}{5}x^5 \loi
\end{bmatrix}
$$
$$
\begin{bmatrix}
2\alpha & 0 & | & 0 \\
0 & \dfrac{2}{3}\alpha^3 & | & \dfrac{4}{5}\alpha^5 \\ 
\end{bmatrix}
$$
Using row matrix operations leads to $\pi_1=\dfrac{6}{5}\alpha^2$.
Thus $\hat\varphi=\dfrac{6}{5}\alpha^2x$.
## Relation to [[XTX & XTY Method]]
$$
A = X^TX; B = X^TY
$$