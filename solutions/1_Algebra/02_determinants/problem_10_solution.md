## Question

Exercise 10. Detecting Dependence
Without carrying out a full determinant calculation, explain why:
$\det([1\ 2\ 3;\ 2\ 4\ 6;\ 0\ 1\ 5]) = 0$.
Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.
*(Why this exercise: teaches how to recognize a zero determinant from the structure of a matrix.)*

## Solution

1. **Analyzing the Row Structure:**
Let the rows of the matrix be designated as:
* $R_1 = [1\ 2\ 3]$
* $R_2 = [2\ 4\ 6]$
* $R_3 = [0\ 1\ 5]$


2. **Identifying Linear Dependence:**
By inspecting the first two rows, we can see that the second row is an exact scalar multiple of the first row:
$R_2 = 2R_1 \quad (\text{since } 2 \times 1 = 2,\ 2 \times 2 = 4,\ 2 \times 3 = 6)$
Because one row can be expressed as a linear combination of another, the rows of the matrix are **linearly dependent**.
3. **Connecting to a Zero Determinant:**
A core property of determinants states that if a square matrix has linearly dependent rows or columns, its determinant is automatically zero. Since $R_2$ is a multiple of $R_1$, the rows do not span a full 3-dimensional volume, immediately yielding $\det(A) = 0$ without requiring any cofactor expansion or full calculation.
4. **Connection to Noninvertibility:**
A square matrix is invertible if and only if its determinant is non-zero (equivalently, if its rows are linearly independent). Because $\det(A) = 0$, the matrix is **not invertible** (singular). Geometrically, the transformation represented by this matrix collapses 3D space into a lower dimension (flattening it onto a plane), which destroys information and makes it impossible to reverse.
