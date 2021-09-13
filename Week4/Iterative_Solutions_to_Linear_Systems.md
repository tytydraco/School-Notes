# Iterative Solutions to Linear Systems

## Jacobi Method
- Assume all diagonal elements are nonzero
  - If not the case; arrange for this
![](img/jacobi.png)
- Consider x0 = [0, 0, 0, ...]
- The more iterations, the more accurate

## Gauss-Seidel Method
- Use Jacobi Method but use x^k instead of x^(k-1)
![](img/gauss_seidel.png)
- Takes less iterations to solve

## Gauss-Seidel w/ SOR
- Add a relaxation factor (w)
![](img/gauss_seidel_sor.png)
- If w = 1, equivalent to [Gauss-Seidel Method](##-Gauss-Seidel-Method)

## Convergence
- To converge starting vector, coefficient matrix
![](img/convergence.png)

## Convergence Error Check
- Error = || x^k - x^(k-1) || / || x^k ||