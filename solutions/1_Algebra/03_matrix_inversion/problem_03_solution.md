## Question

Exercise 3. When Does the Inverse Not Exist?
For:
A = [2 4; 1 2]
explain in two ways why A⁻¹ does not exist: using the determinant and using dependence between the rows.

## Solution

1. **Method 1: Using the Determinant**
* For a 2 × 2 matrix [a b; c d], the determinant is given by $ad - bc$.
* Applying this formula to matrix A = [2 4; 1 2]:
det(A) = (2 × 2) - (4 × 1) = 4 - 4 = 0.
* **Explanation:** A square matrix is invertible if and only if its determinant is non-zero. Because $\det(A) = 0$, division by the determinant is undefined, which means the inverse matrix $A^{-1}$ does not exist (the matrix is singular).


2. **Method 2: Using Dependence Between the Rows**
* Let the rows of matrix A be designated as:
* Row 1: $R_1 = [2\ 4]$
* Row 2: $R_2 = [1\ 2]$


* By inspection, the first row is an exact scalar multiple of the second row ($R_1 = 2R_2$), which means the rows are **linearly dependent**.
* **Explanation:** Linearly dependent rows indicate that the matrix collapses 2D space onto a 1-dimensional line during transformation. Because information is irretrievably lost in this collapse, the transformation cannot be reversed or undone, confirming that the inverse cannot exist.
