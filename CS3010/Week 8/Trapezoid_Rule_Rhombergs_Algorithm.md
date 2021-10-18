# Integration With Trapezoid Method

## Newton-Cotes Integration
- Replace a difficult to integrate function with an approximated, easier one

## Trapezoidal Rule
- Case when polynomial is first-order
- I = (b - a)[(f(a) + f(b))/2]
- To improve it's accuracy, we can do this method for multiple segments
  - Instead of from [0,10], maybe [0,1], [1,2], [2,3], etc
  - Chain together multiple trapezoidal rules
- If we use equidistant partitions, we can shorten this formula!
  - Assume h = (b - a) / n
  - n = number of points minus 1
  - h should remain the same then
  - h/2 * sum from 0 to n-1 of [f(x_i) + f(x_i+1)]

## Error
- Error = -( (b - a) / 12 ) * h^2 * f''(e)
