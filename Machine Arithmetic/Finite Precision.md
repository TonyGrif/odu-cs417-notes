---
tags:
  - Error-Metric
---
# Finite Precision
Computers must operate with a set [[Prerequisite Math#Machine Precision| machine precision]] and cannot store every number.
## Storage Criteria
1. Can we store the whole number?
    * If this falls within our available precision, store it all.
    * If it falls without of our available precision, we would have an [[Prerequisite Math#Storage | error]] trying to store it all.
2. Do we [[Prerequisite Math#Rounding | round]]?
## Notation
* Infinite Precision: $x * \beta^{e}$
* Finite Precision: $x^{*} * \beta^{e^{*}}$
Where $x$ is the number of mantissa bits, $\beta$ is the base, $e$ is the exponent, and $^*$ represents there exists error.
## Error
To determine the error that occurs in the storage of a number, you must calculate either the relative or absolute [[Prerequisite Math#Error Metrics | error]]. 
### Worst Case
The worst case absolute error is $\beta^{-t} * \beta^e$; the worst case relative error is $\beta^{-t+1}$; $t$ is equal to the number of mantissa bits allowed for.