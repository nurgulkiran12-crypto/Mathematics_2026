## Question

Exercise 2. Formula for a 2×2 Matrix
Find the inverse of:
A = [3 2; 5 4]
using the formula for a 2×2 matrix. At the end, check the result by computing one product with A.

## Solution

1. **Computing the Determinant of A:**
* For a 2 × 2 matrix [a b; c d], the determinant is given by $ad - bc$.
* Applying this to matrix A = [3 2; 5 4]:
det(A) = (3 × 4) - (2 × 5) = 12 - 10 = 2.
* Since det(A) = 2 (which is non-zero), the matrix is invertible, and its inverse exists.


2. **Applying the 2×2 Inverse Formula:**
* The formula for the inverse of a 2 × 2 matrix is:
A⁻¹ = (1 / det(A)) * [d -b; -c a]
* Swapping the main diagonal entries ($3$ and $4$), negating the off-diagonal entries ($-2$ and $-5$), and dividing by the determinant ($2$):
A⁻¹ = (1 / 2) * [4 -2; -5 3] = [2 -1; -5/2 3/2] (written in decimal form as [2 -1; -2.5 1.5]).


3. **Checking the Result by Computing A * A⁻¹:**
* Multiplying our original matrix A by the computed inverse A⁻¹:
A * A⁻¹ = [3 2; 5 4] * [2 -1; -2.5 1.5]
* Performing the matrix multiplication:
A * A⁻¹ = [(3 × 2) + (2 × -2.5), (3 × -1) + (2 × 1.5); (5 × 2) + (4 × -2.5), (5 × -1) + (4 × 1.5)]
A * A⁻¹ = [6 - 5, -3 + 3; 10 - 10, -5 + 6]
A * A⁻¹ = [1 0; 0 1]
* **Conclusion:** Because the product yields the 2 × 2 identity matrix, our calculated inverse is verified as completely correct.
