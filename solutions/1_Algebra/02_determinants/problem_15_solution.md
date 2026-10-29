## Question

Exercise 15. Combining Determinant Properties
Let A and B be invertible 2 × 2 matrices with:
det(A) = -2, det(B) = 3
Without finding the entries of the matrices, compute:
det(B⁻¹ Aᵀ B)
State the determinant properties you use in order and explain why the factors involving B eventually cancel.

## Solution

1. **Applying Determinant Properties Step-by-Step:**
* **Step 1 (Multiplicative Property):** The determinant of a product of matrices is equal to the product of their individual determinants ($\det(XYZ) = \det(X) \times \det(Y) \times \det(Z)$).
$\det(B^{-1} A^T B) = \det(B^{-1}) \times \det(A^T) \times \det(B)$
* **Step 2 (Determinant of an Inverse):** The determinant of an inverse matrix is the reciprocal of the original matrix's determinant ($\det(B^{-1}) = \frac{1}{\det(B)}$).
$\det(B^{-1} A^T B) = \frac{1}{\det(B)} \times \det(A^T) \times \det(B)$
* **Step 3 (Determinant of a Transpose):** The determinant of a transpose equals the determinant of the original matrix ($\det(A^T) = \det(A)$).
$\det(B^{-1} A^T B) = \frac{1}{\det(B)} \times \det(A) \times \det(B)$


2. **Computing the Value:**
* Substitute the given values ($\det(A) = -2$ and $\det(B) = 3$):
$\det(B^{-1} A^T B) = \frac{1}{3} \times (-2) \times 3$
* Simplifying the expression:
$\det(B^{-1} A^T B) = -2$


3. **Explanation of Why the Factors Involving B Cancel:**
* The terms involving $B$ appear as $\det(B^{-1})$ and $\det(B)$, which evaluate to $\frac{1}{\det(B)}$ and $\det(B)$ respectively.
* When multiplied together, $\frac{1}{\det(B)} \times \det(B) = 1$. Geometrically, matrix $B$ scales the volume of space by a factor of 3, while its inverse $B^{-1}$ scales it back down by $\frac{1}{3}$. Because these two transformation effects directly undo each other, they completely cancel out, leaving only the scaling effect of matrix $A$ (via its transpose).
