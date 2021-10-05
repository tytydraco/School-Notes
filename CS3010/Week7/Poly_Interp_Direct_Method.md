# Polynomial Interpolation - Direct Method
- Given x and f(x) values, find a polynomial that fits it
- Form:
  - f(x_0) = a_0
  - f(x_1) = a_0 + a_1(x_1 - x_0)
  - f(x_2) = a_0 + a_1(x_2 - x_0) + a_2(x_2 - x_0)(x_2 - x_1)
  - ...
- Example:
- Given points:
  - (0, -5)
  - (1, -3)
  - (-1, -15)
  - (2, 39)
  - (-2, -9)
- p_0(x) = -5
- p_1(x) = p_0(x) + c(x - x_0)
- p_1(x) = -5 + c(x - 0)
- We need to find c!
  - We already know that p_(1) = -3, so substitute 1 for x
  - p_1(1) = -5 + c(1 - 0)
  - -3 = -5 + c
  - c = 2
- p_1(x) = -5 + 2x
- p_2(x) = p_1(x) + c(x - x_0)(x - x_1)
- p_2(x) = -5 + 2x + c(x - 0)(x - x_1)
- We need to find c again!
  - p_2(-1) = -15
  - -15 = -5 + 2(-1) + c(-1 - 0)(-1 - 1)
  - -15 = -7 + c(-1)(-2)
  - -15 = -7 + 2c
  - -8 = 2c
  - c = -4
- p_2(x) = -5 + 2x - 4x(x-1)

## Nested form
- p(x) = a_0 + (x - x_0)(a_1 + (x - x_1)(a_2 + ... (x - x_n-1)a_n))

# Newton's Divided-Difference
- f_1(x) = f(x_0) + (f(x_1) - f(x_0)) / (x_1 - x_0) * (x - x_0)

# Quadratic Interpolation
- f_2(x) = a_0 + a_1(x - x_0) + a_2(x - x_0)(x - x_1)
- To determine coefficients:
  - a_0 = f(x_0)
  - a_1 = (f(x_1) - f(x_0)) / (x_1 - x_0)
  - ...
