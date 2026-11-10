## Question

Exercise 6. Solving a System Using the Inverse
Solve:
Ax = b,
where:
A = [2 1; 1 3], b = [5; 7]
using x = A⁻¹b. Then substitute the resulting vector back into the equation and check the result.

## Solution

1. **Finding the Inverse of Matrix A:**
* First, compute the determinant of matrix A = [2 1; 1 3]:
det(A) = (2 × 3) - (1 × 1) = 6 - 1 = 5.
* Since det(A) = 5 (which is non-zero), the matrix is invertible.
* Using the 2 × 2 inverse formula (A⁻¹ = (1 / det(A)) * [d -b; -c a]):
A⁻¹ = (1 / 5) * [3 -1; -1 2] = [3/5 -1/5; -1/5 2/5] (or in decimal form: [0.6 -0.2; -0.2 0.4]).


2. **Computing the Solution Vector x = A⁻¹b:**
* Multiply the inverse matrix A⁻¹ by the right-hand side vector b = [5; 7]:
x = [3/5 -1/5; -1/5 2/5] * [5; 7]
* Calculating each component:
* x₁ = (3/5 × 5) + (-1/5 × 7) = 3 - (7/5) = (15/5) - (7/5) = 8/5 = 1.6
* x₂ = (-1/5 × 5) + (2/5 × 7) = -1 + (14/5) = (-5/5) + (14/5) = 9/5 = 1.8


* Therefore, the solution vector is **x = [1.6; 1.8]** (or [8/5; 9/5]).


3. **Checking the Result by Substituting Back into Ax = b:**
* Substitute our solution x back into the original matrix equation A * x:
[2 1; 1 3] * [1.6; 1.8]
* Evaluating row by row:
* Row 1: (2 × 1.6) + (1 × 1.8) = 3.2 + 1.8 = 5 (Matches b₁)
* Row 2: (1 × 1.6) + (3 × 1.8) = 1.6 + 5.4 = 7 (Matches b₂)


* **Conclusion:** Because the product equals the right-hand side vector b = [5; 7], our solution vector is verified as correct.
