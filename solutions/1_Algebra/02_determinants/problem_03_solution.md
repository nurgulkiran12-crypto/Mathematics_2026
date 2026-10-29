A = [1 2 0; 0 3 1; 2 1 1]

Computing det(A):
Using expansion along the first column:
det(A) = 1 * det([3 1; 1 1]) - 0 + 2 * det([2 0; 3 1])
det(A) = 1 * (3 - 1) + 2 * (2 - 0) = 1(2) + 2(2) = 2 + 4 = 6

Forming matrix B:
Swapping the first and second rows of A:
B = [0 3 1; 1 2 0; 2 1 1]

Predicting det(B):
Property: Swapping any two rows of a matrix multiplies its determinant by -1.
Prediction: det(B) = -det(A) = -6

Verification by calculation:
det(B) = 0 - 3 * det([1 0; 2 1]) + 1 * det([1 2; 2 1])
det(B) = -3 * (1 - 0) + 1 * (1 - 4) = -3(1) + 1(-3) = -3 - 3 = -6
The calculation matches our prediction.
