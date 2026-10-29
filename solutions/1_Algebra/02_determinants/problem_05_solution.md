QuestionExercise 5. Row Operations
For the matrix:
A = [1 2 3; 2 1 0; -1 4 2]
find det(A) by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.SolutionStep-by-step Row Operations:Operation 1: Eliminate the first entry of row 2.Row operation: $R_2 \to R_2 - 2R_1$Effect on determinant: Adding a multiple of one row to another does not change the determinant.New row 2: [0 -3 -6]Operation 2: Eliminate the first entry of row 3.Row operation: $R_3 \to R_3 + R_1$Effect on determinant: Adding a multiple of one row to another does not change the determinant.New row 3: [0 6 5]Matrix becomes:
[1 2 3; 0 -3 -6; 0 6 5]Operation 3: Eliminate the second entry of row 3 to form an upper triangular matrix.Row operation: $R_3 \to R_3 + 2R_2$ (since $6 + 2(-3) = 0$)Effect on determinant: Adding a multiple of one row to another does not change the determinant.New row 3: [0 0 -7]Final Upper Triangular Matrix:
[1 2 3; 0 -3 -6; 0 0 -7]Calculating Final det(A):
Since all performed row operations preserved the determinant value, the determinant of the original matrix is equal to the product of the diagonal entries of the final triangular matrix:
det(A) = 1 × (-3) × (-7) = 21
