---
tags:
  - Error-Metric
---
# Weighted L2-Norm
The weighted L2-norm is utilized to calculate [[Least-Squares Approximation Overview | least-squares]] error metric.
## Equation
$E^2(\varphi_n) = ||f(x)-\hat{\varphi}(x)||^2 =\int_{\mathbb{R}} \varphi_n^2 d \lambda - 2\int_{\mathbb{R}} \varphi_n f d \lambda + \int_{\mathbb{R}} f^2 d \lambda$ 