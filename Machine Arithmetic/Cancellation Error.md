---
tags:
  - Error-Metric
---
# Cancellation Error
This occurs **only** when two "big" numbers are subtracted and yield a number smaller by orders of magnitude. This can be mitigated by removing the problematic subtraction.
## Steps for Mitigation
1. Multiply by the conjugate
2. Combine fractions
3. *Maybe*, get rid of division
4. Split numerator

**NOTE**: The resulting equation must, for a given input, have the same output as the original function.
## Example
$$\sqrt{1+x^2}-1, |x|\approx0$$
$$(\sqrt{1+x^2}-1)\dfrac{\sqrt{1+x^2}+1}{\sqrt{1+x^2}+1}=\dfrac{x^2}{\sqrt{1+x^2}+1}$$
Subtraction is removed; thus, the cancellation error has been mitigated.