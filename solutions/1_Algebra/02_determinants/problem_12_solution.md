## Question

Exercise 12. A Parameter Revealed by a Row Operation
For:
A(t) = [1 2 3; 2 4 t; 0 1 1]
find the values of t for which the matrix is not invertible.
Before computing the determinant, perform the operation:
$R_2 \leftarrow R_2 - 2R_1$
and use the resulting structure. At the end, explain what special thing happens to the rows for the value of the parameter you found.

## Solution

1. **Initial Matrix A(t):**
A(t) = [1 2 3; 2 4 t; 0 1 1]
2. **Performing the Row Operation ($R_2 \leftarrow R_2 - 2R_1$):**
* We subtract 2 times the first row from the second row to simplify the matrix:
* New row 2: [2 - 2(1), 4 - 2(2), t - 2(3)] = [2 - 2, 4 - 4, t - 6] = [0, 0, t - 6]


* Matrix after the row operation:
[1 2 3; 0 0 t - 6; 0 1 1]


3. **Computing the Determinant:**
* We can expand the determinant along the first column, which already has two zeros, or use a row swap (note that swapping rows changes the sign of the determinant, but since we are setting it to zero, it does not affect our final values):
Using cofactor expansion along the first column:
$\det(A(t)) = 1 \times \det([0\ t-6;\ 1\ 1]) - 0 + 0$
$\det(A(t)) = 1 \times (0 \times 1 - (t - 6) \times 1) = -(t - 6) = 6 - t$


4. **Finding Values of t for Which the Matrix Is Not Invertible:**
* A square matrix is **not invertible** (singular) if and only if its determinant is equal to zero.
* Setting our determinant equal to zero:
$6 - t = 0 \implies t = 6$
* Therefore, the matrix is not invertible when **t = 6**.


5. **Explanation of the Special Row Structure:**
* When $t = 6$, substituting it back into our matrix after the row operation yields the second row as `[0 0 0]`.
* **Special occurrence:** Having an entire row of zeros means that the rows of the matrix become **linearly dependent** (specifically, a zero row is a trivial linear combination of other rows). Geometrically, this means the linear transformation collapses the 3-dimensional space onto a lower-dimensional flat plane, destroying volume and information, which directly explains why the matrix cannot be inverted.
