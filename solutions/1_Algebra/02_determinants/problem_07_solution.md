## Question

Exercise 7. Using Properties Instead of Recomputing
Suppose that for a 3 × 3 matrix, det(A) = -4. Compute:
$\det(2A), \det(A^T), \det(A^2), \det(-A)$.
Justify each answer using the appropriate property.

## Solution

1. **Computing $\det(2A)$:**
* **Property:** For any $n \times n$ matrix $A$ and scalar $c$, scaling the matrix scales its determinant by $c^n$, meaning $\det(cA) = c^n \det(A)$.
* **Calculation:** Since matrix $A$ is of size $3 \times 3$ (so $n = 3$) and the scalar is $c = 2$:
$\det(2A) = 2^3 \times \det(A) = 8 \times (-4) = -32$.


2. **Computing $\det(A^T)$:**
* **Property:** The determinant of a matrix's transpose is always equal to the determinant of the original matrix: $\det(A^T) = \det(A)$.
* **Calculation:**
$\det(A^T) = -4$.


3. **Computing $\det(A^2)$:**
* **Property:** The determinant of a product is multiplicative, such that $\det(XY) = \det(X) \times \det(Y)$. Therefore, $\det(A^2) = (\det(A))^2$.
* **Calculation:**
$\det(A^2) = (-4)^2 = 16$.


4. **Computing $\det(-A)$:**
* **Property:** Multiplying a matrix by $-1$ follows the scalar multiplication rule $\det(cA) = c^n \det(A)$ with $c = -1$. For an $n \times n$ matrix, $\det(-A) = (-1)^n \det(A)$.
* **Calculation:** Since $n = 3$ is odd, $(-1)^3 = -1$:
$\det(-A) = (-1)^3 \times \det(A) = -1 \times (-4) = 4$.
