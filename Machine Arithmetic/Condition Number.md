---
tags:
  - Error-Metric
---
# Condition Number
The condition number determines the amount of impact [[Prerequisite Math#Relative Error| error]] ($\varepsilon$) has on the result. When the resulting number if **approximately** one, the result is good; anything **greater than** one is bad. A condition number of zero means the input has no effect on the output.
## Equation
$$\def\con{cond \ f} (\con)(x)=|\dfrac{xf^{'}(x)}{f(x)}|$$

## Example
$$f(x)=\dfrac{x^3+1x^2-1}{x^2+5}$$
Using calculus' chain rule to skip to $\dfrac{f^{'}(x)}{f(x)}$... $$\dfrac{f^{'}(x)}{f(x)} = \dfrac{d}{dx}ln(\dfrac{x^3+2x^2-1}{x^2+5})=\dfrac{d}{dx}ln(x^3+2x^2-1)-\dfrac{d}{dx}ln(x^2+5)$$
$$\dfrac{f^{'}(x)}{f(x)}=\dfrac{3x^2+4x}{x^3+2x^2-1}-\dfrac{2x}{x^2+5}$$
Where $|x| \approx 0$...
$$|\dfrac{xf^{'}(x)}{f(x)}|=|\dfrac{2x^3+4x^2}{x^3+2x^2-1}-\dfrac{2x^2}{x^2+5}|=|\approx0-\approx0|$$
Thus, this problem is **well-conditioned**.

**NOTE**: The [[Cancellation Error | cancellation error]] implies nothing about the condition number; they are related analyses, but they have no impact on each other.