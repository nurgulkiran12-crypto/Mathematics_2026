## Question

Exercise 11. Parameter and Invertibility
For:
A(t) = [1 t; t 1]
find all t for which the matrix is invertible, and then give a formula for A(t)⁻¹. Explain what happens to this formula at the excluded values.

## Solution

1. **Finding the Determinant and Invertible Range:**
* Compute the determinant of matrix A(t) = [1 t; t 1]:
det(A(t)) = (1 × 1) - (t × t) = 1 - t²
* A square matrix is invertible if and only if its determinant is non-zero:
1 - t² ≠ 0 => t² ≠ 1 => t ≠ 1 and t ≠ -1.
* Therefore, the matrix is invertible for **all real numbers t except t = 1 and t = -1**.


2. **Finding the Formula for A(t)⁻¹:**
* Using the 2 × 2 inverse formula (A⁻¹ = (1 / det(A)) * [d -b; -c a]):
A(t)⁻¹ = (1 / (1 - t²)) * [1 -t; -t 1]


3. **Explaining What Happens at the Excluded Values:**
* At the excluded values **t = 1** and **t = -1**, the denominator (1 - t²) becomes zero.
* Division by zero is undefined, causing the scalar multiplier and formula values to blow up to infinity, which confirms that the inverse does not exist.
* Geometrically, substituting $t = 1$ gives [1 1; 1 1], where the rows are identical and linearly dependent. This means the linear transformation collapses 2D space onto a 1-dimensional line, destroying information and making it impossible to undo or invert.
