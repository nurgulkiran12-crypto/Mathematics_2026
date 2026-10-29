## Question

Exercise 1. Determinant of a 2×2 Matrix
Compute:
$\det([3\ -2;\ 5\ 4])$ and $\det([1\ 7;\ 2\ 14])$.
Which matrix is invertible? Justify your answer.
*(Why this exercise: introduces the simplest determinant calculation and immediately connects it with invertibility.)*

## Solution

1. **Computing the Determinant of the First Matrix ($A = [3\ -2;\ 5\ 4]$):**
* For a 2 × 2 matrix $[a\ b;\ c\ d]$, the determinant is given by $ad - bc$.
* Applying the formula:
$\det(A) = (3 \times 4) - (-2 \times 5) = 12 - (-10) = 12 + 10 = 22$.


2. **Computing the Determinant of the Second Matrix ($B = [1\ 7;\ 2\ 14]$):**
* Applying the determinant formula:
$\det(B) = (1 \times 14) - (7 \times 2) = 14 - 14 = 0$.


3. **Determining Which Matrix Is Invertible and Why:**
* A square matrix is **invertible** if and only if its determinant is non-zero ($\det \neq 0$).
* **Matrix A** has a determinant of $22$ (which is $\neq 0$), meaning it **is invertible**.
* **Matrix B** has a determinant of $0$, meaning it **is not invertible** (it is singular). Geometrically, this means the columns of matrix B are linearly dependent (the second column is 7 times the first column), so the transformation collapses 2D space onto a line and cannot be reversed.
