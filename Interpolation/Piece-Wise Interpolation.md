---
tags:
  - Interpolation
---
# Piece-Wise Interpolation
[[Interpolation Overview | Interpolate]] a given function on each interval separately.
## Linear
Given a collection of points, calculate the [[Prerequisite Math#Slope | slope]] from one point to the next until you have reached the end. This method uses local information for each subdomain leading to the endpoints are **points of discontinuity**.
## Spline Functions
Unlike linear interpolation methods ([[Lagrange Form | Lagrange form]] and [[Newton's Form | Newton form]]), this method will generate, not a single polynomial of a high degree, but many polynomials of a smaller degree. Unlike [[#Linear | linear piece-wise]], this method will also remove points of discontinuity. 
### Equation
$$
\mathbb{S}_{m}^{k}(\triangle)=\{ s : s\in C^k[a,b],s|_{[x_i,x_{i+1}]} \in \mathbb{P}_m \}
$$
* $\mathbb{S}_m^k(\triangle)$ is the overal spine function with degree $m$ and smoothness class $k$.
* $s$ is one spline function.
* $C^k$ is the smoothness class.
    * This can also be read as "has $k$ derivatives".
    * $k=-1$ if no concavity is required
* $[a,b]$ is the domain $a \leq x \leq b$.
* $s|_{[x_i,x_{i+1}]}$ are each [[#Sub-Splines | sub-splines]].
* $|_{[x_i,x_i+1]}$ defined over the domain $[x_i,x_{i+1}]$.
* $\in \mathbb{P}_m$ defines it belongs to the set of polynomials of degree $m$.
#### Sub-Splines
Each sub-spline is written as:
$$
s_m(f;.) \in \mathbb{S}_m^{m-1}
$$
* $s_m$ represents a polynomial of degree $m$.
* $s, s^{'}, ..., s^{'\times(m-1)}$ are all continuous on $[a,b]$. 

Each sub-spline is defined as:
$$
s_i(x)=c_{i,1}(x-x_1)+c_{i,2}(x-x_1)^2+...c_{i,n}(x-x_1)^n
$$