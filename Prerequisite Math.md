# Binary Conversion
It is necessary for a computer to convert decimal (base-10) numbers into binary (base-2) to be stored.
```
/* Fraction Number */
func convert(float dec) {
    result = (2 * dec)
    if result > 1
        bin += 1
        convert(result - 1)
    else if result == 0
        return bin
    else
        bin += 0
        convert(result)
}
```
# Machine Precision
Computers can only store a number up to a certain point, meaning they have finite precision. 
## Cleve Moler Estimation
This algorithm estimates the machine precision for a given machine data type.
```
let a <- 4.0 / 3.0
let b <- a - 1
let c <- b + b + b
return |1 - c|
```
## Storage
If the number is less than the finite precision of a machine, **underflow** occurs.
If the number is greater than the finite precision of a machine, **overflow** occurs.
# Scientific Notation
When dealing with numbers with a large number of characters, it becomes necessary to use a more concise representation.
$x_{\beta} = \beta^e$
Where $x$ is the real number, $\beta$ is the base, and $e$ is the exponent.
## Normalization Constraint 
1. The first number to the right of the decimal must be non-zero (unless we are representing zero)
2. Everything to the left of the decimal place must be a zero
# Rounding
There are two methods for rounding:
1. Symmetric: the standard rounding, round up or down to the nearest integer
2. Truncation: any characters that cannot be stored are just lopped off
# Error Metrics
There are two types of error metrics.
## Absolute Error
The total amount the actual value is off from the known value.
$$\def\k{known} \def\a{actual} |\k - \a|$$
## Relative Error
Relative error is concerned with how far off the result is from the known value relative to the known.
$$\def\k{known} \def\a{actual} \dfrac{|\k - \a|}{|\k|}$$
# Slope
Calculating the slope between two points is $\dfrac{rise}{run}$ or $\dfrac{y_1-y_0}{x_1-x_0}$. 