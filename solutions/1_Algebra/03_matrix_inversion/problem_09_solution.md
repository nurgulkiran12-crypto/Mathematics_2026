## Question

Exercise 9. Matrix Equation
Given:
A = [1 2; 0 1], B = [3 1; 2 4]
Solve the equation AX = B for X. Before calculating, decide on which side of the equation A⁻¹ must be used. Then check the result by computing AX.

## Solution

1. **Determining Which Side to Apply A⁻¹:**
* Because matrix multiplication is **noncommutative** (meaning order matters and $AX \neq XA$), we must be careful when isolating $X$.
* To solve the equation $AX = B$, we must multiply both sides on the **left** by $A^{-1}$:
$A^{-1}(AX) = A^{-1}B \implies (A^{-1}A)X = A^{-1}B \implies I X = A^{-1}B \implies X = A^{-1}B$.
* Therefore, $A^{-1}$ must be applied on the **left side** of matrix $B$.


2. **Finding the Inverse of Matrix A:**
* For A = [1 2; 0 1], compute the determinant:
det(A) = (1 × 1) - (2 × 0) = 1 - 0 = 1.
* Using the 2 × 2 inverse formula:
A⁻¹ = (1 / 1) * [1 -2; -0 1] = [1 -2; 0 1].


3. **Computing X = A⁻¹B:**
* Multiply $A^{-1}$ by $B = [3\ 1;\ 2\ 4]$:
X = [1 -2; 0 1] * [3 1; 2 4]
* Evaluating row by row:
* Row 1, Col 1: $(1 \times 3) + (-2 \times 2) = 3 - 4 = -1$
* Row 1, Col 2: $(1 \times 1) + (-2 \times 4) = 1 - 8 = -7$
* Row 2, Col 1: $(0 \times 3) + (1 \times 2) = 0 + 2 = 2$
* Row 2, Col 2: $(0 \times 1) + (1 \times 4) = 0 + 4 = 4$


* Therefore, the solution matrix is:
**X = [-1 -7; 2 4]**


4. **Checking the Result by Computing AX:**
* Multiply our original matrix $A$ by the solved matrix $X$:
AX = [1 2; 0 1] * [-1 -7; 2 4]
* Evaluating:
* Row 1, Col 1: $(1 \times -1) + (2 \times 2) = -1 + 4 = 3$
* Row 1, Col 2: $(1 \times -7) + (2 \times 4) = -7 + 8 = 1$
* Row 2, Col 1: $(0 \times -1) + (1 \times 2) = 0 + 2 = 2$
* Row 2, Col 2: $(0 \times -7) + (1 \times 4) = 0 + 4 = 4$


* **Conclusion:** The product yields `[3 1; 2 4]`, which exactly matches our right-hand side matrix $B$, verifying that our solution for $X$ is correct.
