Question
Exercise 3. Swapping Two Rows
For the matrix:
A = [1 2 0; 0 3 1; 2 1 1]
compute det(A). Then form a matrix B by swapping the first and second rows of A. First predict det(B) using a determinant property, and then verify your prediction by calculation.

Solution
Computing det(A):
Using cofactor expansion along the first row:
det(A) = 1 * det([3 1; 1 1]) - 2 * det([0 1; 2 1]) + 0
det(A) = 1 * ((3 × 1) - (1 × 1)) - 2 * ((0 × 1) - (1 × 2))
det(A) = 1 * (3 - 1) - 2 * (0 - 2) = 1 * (2) - 2 * (-2) = 2 + 4 = 6

Forming matrix B by swapping rows 1 and 2:
B = [0 3 1; 1 2 0; 2 1 1]

Predicting det(B) using a determinant property:
Property: If two rows of a matrix are swapped, the determinant changes sign.
Prediction: Since det(A) = 6, we predict that det(B) = -6.

Verification by calculation:
Expanding det(B) along the first row:
det(B) = 0 * (...) - 3 * det([1 0; 2 1]) + 1 * det([1 2; 2 1])
det(B) = -3 * ((1 × 1) - (0 × 2)) + 1 * ((1 × 1) - (2 × 2))
det(B) = -3 * (1 - 0) + 1 * (1 - 4) = -3 * (1) + 1 * (-3) = -3 - 3 = -6

The calculated determinant matches our prediction (det(B) = -6).
