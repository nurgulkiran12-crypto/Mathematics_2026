## Question

Exercise 8. Determinant of a Product
Let A, B be square matrices such that det(A) = 3 and det(B) = -5. Compute det(AB), det(BA) and, if it exists, det(A⁻¹B). Explain why the first two results are equal even though usually AB ≠ BA.

## Solution

1. **Computing det(AB):**
* **Property:** The determinant of a matrix product is equal to the product of their individual determinants: $\det(AB) = \det(A) \times \det(B)$.
* **Calculation:**
$\det(AB) = 3 \times (-5) = -15$.


2. **Computing det(BA):**
* **Property:** Applying the same multiplicative property: $\det(BA) = \det(B) \times \det(A)$.
* **Calculation:**
$\det(BA) = -5 \times 3 = -15$.


3. **Computing det(A⁻¹B):**
* **Existence Check:** Since $\det(A) = 3 \neq 0$, matrix $A$ is invertible, which guarantees that $A^{-1}$ exists.
* **Property:** $\det(A^{-1}B) = \det(A^{-1}) \times \det(B) = \frac{1}{\det(A)} \times \det(B)$.
* **Calculation:**
$\det(A^{-1}B) = \frac{1}{3} \times (-5) = -\frac{5}{3}$.


4. **Explanation of Why det(AB) = det(BA):**
* Although matrix multiplication is **noncommutative** (meaning $AB \neq BA$ in general), determinants yield ordinary scalar numbers.
* Because real numbers commute under multiplication, $\det(A) \times \det(B)$ is guaranteed to equal $\det(B) \times \det(A)$ ($3 \times -5 = -5 \times 3$). Therefore, the scalar determinants of $AB$ and $BA$ are always equal, even though the underlying matrices themselves are different.
