Question
For the matrix:
A = [1 2 -1; 0 3 4; 2 1 5]
compute det(A) using Sarrus' rule. Then perform one simple check using a chosen property of indices or cofactor expansion.

Solution
Computing det(A) using Sarrus' rule:
Copying the first two columns to the right:
[1  2 -1 | 1  2]
[0  3  4 | 0  3]
[2  1  5 | 2  1]

Main diagonals (down-right):
(1 * 3 * 5) + (2 * 4 * 2) + (-1 * 0 * 1) = 15 + 16 + 0 = 31

Anti-diagonals (down-left):
(2 * 3 * -1) + (1 * 4 * 1) + (5 * 0 * 2) = -6 + 4 + 0 = -2

Determinant = (Sum of main diagonals) - (Sum of anti-diagonals)
det(A) = 31 - (-2) = 31 + 2 = 33

Verification Check (Cofactor Expansion along Column 1):
To check our work, we expand along the first column (which contains a 0):
det(A) = 1 * det([3 4; 1 5]) - 0 * det([2 -1; 1 5]) + 2 * det([2 -1; 3 4])
det(A) = 1 * ((3 × 5) - (4 × 1)) - 0 + 2 * ((2 × 4) - (-1 × 3))
det(A) = 1 * (15 - 4) + 2 * (8 - (-3))
det(A) = 1 * (11) + 2 * (11) = 11 + 22 = 33

Both methods yield 33, confirming the result is correct
