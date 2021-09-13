# Gaussian Elimination
- Goal is to convert to upper triangular form
- Several methods, for n <= 3, use first three methods

## Graphical method
- For two linear SOE (system of equations), solve both for x2
  - Ex: a<sub>11</sub>x<sub>1</sub> + a<sub>12</sub>x<sub>2</sub> = b<sub>1</sub>
  - x2 = -(a11/a12)x1 + (b1/a12)
  - x2 = -(a12/a22)x1 + (b2/a22)
- This puts it in the form x2 = (slope)x2 + intercept
  - Aka: y = mx + b
- Find where these lines intersect via [Desmos](https://www.desmos.com/)

### Special cases
- No solution (no intersection)
- Infinite solutions (full intersections)
- Difficult to find point of intersection visually

## Cramer's rule
- Determinant: [A]x = [b]
  - A: Coefficient matrix
  - x: Column vector
  - b: Column vector
  - For [A] = [a11], D = a11
  - For [A] = [a11 a12 | a21 a22], D = a11 * a22 = a21 * a12
    - Top left * bot right - bot left * top right
  - For [A] = 3x3 matrix, we cross out the entire top row, and take turns crossing out a column and doing 2x2 determinants with the non-crossed variables
    - For each 2x2 determinant, we multiply by the coefficient in the top row (crossed out row) in which we crossed the column of
    - The second determinant is always negative

## Method of elimination
- Goal is to solve one of the equations for one unknown, and to eliminate that variable from the other equations via substitution
- Ideal for more than 2/3 equations, but becomes tedious when done by hand

### Naive Gauss elimination
- Extension of [Method of elimination](#-Method-of-elimination)
- Two phase solve
  - Forward elimination of unknowns; matrix of upper triangular form
  - Back substitution
- First equation is called pivot equation
- First element is called pivot element

#### Steps
1) Take first equation and transform all subsequent equations such that when subtracted, a variable disappears from all but the first equation
2) Do the same thing for the next equation, ignoring the first equation
3) Continue until left with a single variable in the last equation
4) We now solve for the variable in the last equation, and substitute it into the previous equation
5) Continue until first equation is fully complete
6) Results in all variables being solved

#### Special cases
- Division by zero is possible
- Causes rounding errors
- Small changes in coefficients can result in large solution changes

### Gauss Jordan method
- Variation of [Gaussian elimination](##-Method-of-elimination)

#### Differences
- When a variable is eliminated, it is eliminated for all equations, not just the equation prior
- Rows are normalized by dividing by the pivot element
- Results in an identity matrix
- No need for back substitution

## Computer methods