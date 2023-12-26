---
tags:
  - Approximation
  - Interpolation
---
# Least Squares vs. Interpolation
[[Least-Squares Approximation Overview| Least-squares approximation]] and [[Interpolation Overview | interpolation]] share the end goal of creating an approximation function. The difference comes from interpolation's [[Interpolation Overview#Common Constraint | constraint]]. None of the least-squares approximation methods have this constraint.

Due to this, least-squares approximation can be a polynomial of any degree less than or equal to $n-1$ of the original function. Interpolation's degree must be equal to $n-1$ only.

Least-squares is also a single method, whereas interpolation is a collection of methods.
## Use Cases
Favor [[Least-Squares Approximation Overview | least-squares approximation]] when:
* Capturing global behavior

Favor [[Interpolation Overview | interpolation]] when:
* Capturing local behavior
* Must preserve all input data