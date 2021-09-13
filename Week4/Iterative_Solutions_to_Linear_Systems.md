# Iterative Solutions to Linear Systems

## Jacobi Method
- Assume all diagonal elements are nonzero
  - If not the case; arrange for this
![](img/jacobi.png)
- Consider x0 = \[0, 0, 0, ...\]
- The more iterations, the more accurate
- Basically, that fancy sum function is just what you get when you isolate your variable
  - Ex: 7a + 1b -1c + 2d = 3
  - Solve for a = (3 - b + c - 2d)/7
  - Raise variables to the k power (aka, the value at the previous solution)

## Gauss-Seidel Method
- Use Jacobi Method but use x^k instead of x^(k-1)
![](img/gauss_seidel.png)
- Takes less iterations to solve
- Same as the Jacobi, except when it comes to the last x (i.e. x3), instead of x3^k, you use x2^(k+1)
  - x2^(k+1) is the term we JUST calculated right before

## Gauss-Seidel w/ SOR
- Add a relaxation factor (w)
![](img/gauss_seidel_sor.png)
- If w = 1, equivalent to [Gauss-Seidel Method](##-Gauss-Seidel-Method)
- Same as Gauss-Seidel, just with an added weight variable

## Convergence
- To converge starting vector, coefficient matrix
![](img/convergence.png)

## Convergence Error Check
- Error = || x^k - x^(k-1) || / || x^k ||
