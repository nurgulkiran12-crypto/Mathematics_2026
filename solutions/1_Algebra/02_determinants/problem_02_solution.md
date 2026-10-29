## Question

Exercise 2. Determinant of a 3×3 Matrix
For:
A = [1 2 -1; 0 3 4; 2 1 5]
compute det(A) using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

## Solution

1. **Computing det(A) Using Sarrus' Rule:**
* Append the first two columns to the right of the matrix for the diagonal products:
[1  2 -1 | 1  2]
[0  3  4 | 0  3]
[2  1  5 | 2  1]
* Sum of the products of the main diagonals (going down-right):
$(1 \times 3 \times 5) + (2 \times 4 \times 2) + (-1 \times 0 \times 1) = 15 + 16 + 0 = 31$
* Sum of the products of the secondary diagonals (going up-right):
$(2 \times 3 \times -1) + (1 \times 4 \times 1) + (5 \times 0 \times 2) = -6 + 4 + 0 = -2$
* Subtract the secondary sum from the main sum:
$\det(A) = 31 - (-2) = 31 + 2 = 33$.


2. **Performing a Check Using Cofactor Expansion:**
* **Method:** We can verify our result using cofactor expansion along the first column (which contains a convenient zero) to ensure consistency.
* **Calculation:**
$\det(A) = 1 \times \det([3\ 4;\ 1\ 5]) - 0 \times \det([2\ -1;\ 1\ 5]) + 2 \times \det([2\ -1;\ 3\ 4])$
$\det(A) = 1 \times ((3 \times 5) - (4 \times 1)) - 0 + 2 \times ((2 \times 4) - (-1 \times 3))$
$\det(A) = 1 \times (15 - 4) + 2 \times (8 - (-3))$
$\det(A) = 1 \times 11 + 2 \times 11 = 11 + 22 = 33$.
* **Conclusion:** Both methods yield **33**, confirming that our determinant calculation is correct.
