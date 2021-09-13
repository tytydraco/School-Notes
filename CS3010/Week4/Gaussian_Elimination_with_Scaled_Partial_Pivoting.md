# Gaussian Elimination w/ Scaled Partial Pivoting

## Gaussian Elimination Drawbacks
- Diagonal coefficient might be zero (or close to it)
- This leads to division by zero
- We pivot to fix it

## Pivoting
### Partial
- Making the largest element the pivot element
- Pivot row = maximum pivot entry in abs value
- Designated row moved into the pivot position

### Full
- Largest element in **all** rows and columns; then switching
- Pivot entry = maximum entry in the matrix
- Two rows and two columns switched
- *Partial pivoting is significantly less work and does a decent job usually*

## Performing Pivoting
### Partial Example
- 3𝑥𝑥1 − 13𝑥𝑥2 + 9𝑥𝑥3 + 3𝑥𝑥4 = −19
- −6𝑥𝑥1 + 4𝑥𝑥2 + 𝑥𝑥3 − 18𝑥𝑥4 = −34
- 6𝑥𝑥1 − 2𝑥𝑥2 + 2𝑥𝑥3 + 4𝑥𝑥4 = 16
- 12𝑥𝑥1 − 8𝑥𝑥2 + 6𝑥𝑥3 + 10𝑥𝑥4 = 26
  - l = [1, 2, 3, 4] (xx1, xx2, xx3, xx4)
  - s = [13, 18, 6, 12]
    - Highest coefficients in each row; ordered
  - To deretmine pivot row, take the **first** entry of each row and divide it by that row's largest entry
    - Ex: For first row, 3/13 = 0.23
    - We select the **first** occurance of the largest ratio
      - I.e. if 0.1 shows up twice, we pick the first occurance
  - Row 3 is the pivot equation as it has the largest ratio of 0.1
  - Now switch the rows so that this pivot equation shows up first
    - New l = [**3**, 2, **1**, 4]
  - Repeat process for next step after eliminating a row (?)
