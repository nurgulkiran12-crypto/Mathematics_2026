## Question

Exercise 14. A Matrix That Is Its Own Inverse
Assume that a square matrix A satisfies:
A² = I.
Show that:
A⁻¹ = A.
Then give an example of a 2 × 2 matrix different from I and -I that satisfies this condition, and verify it by multiplication.

## Solution

1. **Showing That A⁻¹ = A:**
* By definition, if a matrix $A$ is multiplied by its inverse $A^{-1}$, the result is the identity matrix ($A \cdot A^{-1} = I$).
* We are given the equation:
$A^2 = I$
* This can be rewritten by expanding the square:
$A \cdot A = I$
* Comparing this directly to the definition of an inverse ($A \cdot A^{-1} = I$), it follows immediately that **$A^{-1} = A$**. (Multiplying $A$ by itself yields $I$, meaning $A$ acts as its own inverse).


2. **Providing an Example of a 2 × 2 Matrix:**
* Let us choose the permutation matrix:
A = [0 1; 1 0]
* This matrix is clearly different from the identity matrix $I = [1 0; 0 1]$ and its negative $-I = [-1 0; 0 -1]$.


3. **Verifying by Multiplication (A² = I):**
* Multiply matrix $A$ by itself:
A² = [0 1; 1 0] * [0 1; 1 0]
* Evaluating row by row:
* Row 1, Col 1: $(0 \times 0) + (1 \times 1) = 0 + 1 = 1$
* Row 1, Col 2: $(0 \times 1) + (1 \times 0) = 0 + 0 = 0$
* Row 2, Col 1: $(1 \times 0) + (0 \times 1) = 0 + 0 = 0$
* Row 2, Col 2: $(1 \times 1) + (0 \times 0) = 1 + 0 = 1$


* The product yields:
[1 0; 0 1]
* **Conclusion:** Because $A^2 = I$, this verifies that the matrix $A = [0 1; 1 0]$ is indeed its own inverse ($A^{-1} = A$).
