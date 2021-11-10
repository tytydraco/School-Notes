# Eigenvalues and Eigenvectors
- Definition: Av = λv
  - A: matrix
  - v: vector
  - λ: scalar

## Calculating
- Av = λv is equivalent to (A - λl)x = 0
  - Must be singular, therefore Det(A - λl) = 0
- p(λ) = Det(A - λl) = 0
  - Find the zeros
  - Will be degree n polynomial with n roots

## Example
- A = [3,2 | 7,-2]
- p(λ) = Det [3 - λ,2 | 7,-2 - λ]
  - p(λ) = (3 - λ)(-2 - λ) - (2)(7)
  - p(λ) = λ^2 - λ - 20
  - p(λ) = (λ - 5)(λ + 4)       <- factors!
- Solve (A - 5I)x = 0 and (A + 4I)x = 0
  - [-2,2 | 7,-7][x1,x2] = [0,0] -> [1, 1]
  - [7,2 | 7,2][x1,x2] = [0,0] -> [2, -7]
 
 ## 3x3
   - When solving, do it like a gaussian elimination problem
   - Set x_3 to 1 since we only have two equations but three variables
