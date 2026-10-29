Given:
A = [1 2 3; 2 1 0; -1 4 2]

Step-by-step Row Operations:

Operation 1: Eliminate the first entry of row 2.

Rule: R2 -> R2 - 2*R1

Effect on determinant: Adding a multiple of one row to another does not change the determinant.

New row 2: [0 -3 -6]

Operation 2: Eliminate the first entry of row 3.

Rule: R3 -> R3 + R1

Effect on determinant: Adding a multiple of one row to another does not change the determinant.

New row 3: [0 6 5]

Matrix becomes:
[1 2 3; 0 -3 -6; 0 6 5]

Operation 3: Eliminate the second entry of row 3 to make it an upper triangular matrix.

Rule: R3 -> R3 + 2*R2 (since 6 + 2(-3) = 0)

Effect on determinant: Adding a multiple of one row to another does not change the determinant.

New row 3: [0 0 -7]

Final Upper Triangular Matrix:
[1 2 3; 0 -3 -6; 0 0 -7]

Calculating final det(A):
Since row operations preserved the determinant value, the determinant of the original matrix is equal to the product of the diagonal entries of the final triangular matrix:
det(A) = 1 * (-3) * (-7) = 21
