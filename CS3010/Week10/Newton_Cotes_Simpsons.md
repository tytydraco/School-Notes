# Newton Cotes Integration Simpson Rules

## Trapezoid Rule: 2^n
- Find recursive formula for 2^n equal intervals for integral
- Start with n=0, n=1,2,3 until you can generalize it
- h = (b-a)/2^n

## Simpson's Rules

### 1/3 rule
- When second-order polynomial is used
- I = (h/3)[f(x_0) + 4f(x_1) + f(x_2)]
- h = (b-a)/2
- Error: (-1/180)(b - a)(h^4)(f^4(e))
- If divided into segments, must have even segments, odd points

### 3/8 rule
- I = (3h/8)[f(x_0) + 3f(x_1) + 3f(x_2) + f(x_2)]
- h = (b-a)/3
- Error: [-5(b - a)]/6480 * f^4(e)
- For odd segments, even points