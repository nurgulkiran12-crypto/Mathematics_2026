## Question

Exercise 12. Finding Inverses Without Starting from Scratch
It is known that:
A⁻¹ = [2 -1; -3 2]
Without finding A, compute (3A)⁻¹, (Aᵀ)⁻¹, and (A²)⁻¹. Justify each result using the appropriate property.

## Solution

1. **Computing (3A)⁻¹:**
* **Property:** For any scalar $c$ and invertible matrix $A$, scaling a matrix scales its inverse by the reciprocal scalar: $(cA)^{-1} = \frac{1}{c} A^{-1}$.
* **Calculation:** Since $c = 3$, we multiply our given $A^{-1}$ by $\frac{1}{3}$:
(3A)⁻¹ = (1 / 3) * [2 -1; -3 2] = [2/3 -1/3; -1 2/3] (or in decimal form: [0.667 -0.333; -1 0.667]).


2. **Computing (Aᵀ)⁻¹:**
* **Property:** The inverse of a transpose is equal to the transpose of the inverse matrix: $(A^T)^{-1} = (A^{-1})^T$. This means we can transpose $A^{-1}$ directly.
* **Calculation:** Take the transpose of $A^{-1} = [2\ -1;\ -3\ 2]$ by swapping its rows and columns:
* Row 1 becomes column 1, and Row 2 becomes column 2.
(Aᵀ)⁻¹ = [2 -3; -1 2].




3. **Computing (A²)⁻¹:**
* **Property:** The inverse of a matrix power is the power of its inverse: $(A^2)^{-1} = (A^{-1})^2$.
* **Calculation:** Multiply $A^{-1}$ by itself:
(A²)⁻¹ = [2 -1; -3 2] * [2 -1; -3 2]
* Row 1, Col 1: $(2 \times 2) + (-1 \times -3) = 4 + 3 = 7$
* Row 1, Col 2: $(2 \times -1) + (-1 \times 2) = -2 - 2 = -4$
* Row 2, Col 1: $(-3 \times 2) + (2 \times -3) = -6 - 6 = -12$
* Row 2, Col 2: $(-3 \times -1) + (2 \times 2) = 3 + 4 = 7$
(A²)⁻¹ = [7 -4; -12 7].
