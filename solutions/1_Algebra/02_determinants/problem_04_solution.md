A = [2 4 1; 0 -3 5; 0 0 7]

Computing the determinant without expanding:
Since all entries below the main diagonal are zero, this is an upper triangular matrix.
By the triangular matrix rule, the determinant is simply the product of the entries along its main diagonal:
det(A) = 2 * (-3) * 7 = -42

Rule for an Arbitrary Triangular Matrix:
The determinant of any triangular matrix (upper or lower triangular) is equal to the product of its main diagonal entries.

Explanation using this example:
If we performed cofactor expansion down the first column (which contains two zeros), we would get:
det(A) = 2 * det([-3 5; 0 7]) - 0 + 0 = 2 * ((-3)(7) - (5)(0)) = 2 * (-3) * 7 = -42.
Thus, all off-diagonal terms vanish, leaving only the product of the diagonal elements.
