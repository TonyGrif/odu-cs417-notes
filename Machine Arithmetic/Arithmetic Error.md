---
tags:
  - Error-Metric
---
# Arithmetic Error
The error contained in a value with [[Finite Precision | finite precision]] is written as $x^*=x(1+\varepsilon_x)$ where $\varepsilon$ is the [[Prerequisite Math#Error Metrics| relative error]] of the variable $x$.

**Note**: For these analyses, anytime a higher order epsilon term is found (ie $\varepsilon_x * \varepsilon_y$), it goes to zero. 
## Example
Analyze the error of $x^{*} \times y^{*}$ 
### No Operand Error
$$\dfrac{|x^*y^* - xy|}{|xy|}$$
$$x^*y^* = x(1+\varepsilon_x)y(1+\varepsilon_y) = 
xy(1+\varepsilon_xj)(1+\varepsilon_y) = xy(1+\varepsilon_x+\varepsilon_y) =  xy+xy(\varepsilon_x+\varepsilon_y)$$
$$|x^*y^* - xy| = |xy + xy(\varepsilon_x+\varepsilon_y) - xy| = |xy(\varepsilon_x+\varepsilon_y)|$$
$$\dfrac{|x^*y^*-xy|}{|xy|} = \dfrac{|xy(\varepsilon_x+\varepsilon_y)|}{|xy|} = \dfrac{|xy||\varepsilon_x+\varepsilon_y|}{|xy|} = 
|\varepsilon_x+\varepsilon_y|
$$
### With Operand Error
$$\dfrac{|(x^*y^*)^* -xy|}{|xy|}$$
$$(x^*y^*)^*=
(xy(1+\varepsilon_x)(1+\varepsilon_y))(1+\varepsilon_{mult})=
xy(1+\varepsilon_x+\varepsilon_y)(1+\varepsilon_{mult})$$
$$|(x^*y^*)^*-xy|=
xy(1+\varepsilon_x+\varepsilon_y)(1+\varepsilon_{mult}) - xy =
xy(\varepsilon_x+\varepsilon_y+\varepsilon_{mult})$$
$$\dfrac{|(x^*y^*)^*-xy|}{|xy|}=
\dfrac{xy(\varepsilon_x+\varepsilon_y+\varepsilon_{mult})}{|xy|}=
|\varepsilon_x+\varepsilon_y+\varepsilon_{mult}|$$
Given the magnitudes of errors are similar:
$$\varepsilon_{max}=\{{\varepsilon_x, \varepsilon_y, \varepsilon_{mult}}\}$$
The error can then be simplified to $|3\varepsilon_{max}|$
