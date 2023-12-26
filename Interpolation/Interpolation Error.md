---
tags:
  - Error-Metric
---
# Interpolation Error
$$f(x)-p_n(x) = \dfrac{f^{(n+1)} (K(x))}{(n+1)!} \prod_{i=0}^{n}(x-x_i)$$
* $e(x) = f(x) - p(x)$ (do not split terms)
* $n$ is the polynomial degree
* $f^{(n+1)}$ is the $n+1^{th}$ derivative of $f$
* $K(x)$ requires a review of [Rolle's Theorem](https://en.m.wikipedia.org/wiki/Rolle's_theorem)

The error **must** be zero at each of the input points due to the [[Interpolation Overview#Common Constraint | common constraint]].
