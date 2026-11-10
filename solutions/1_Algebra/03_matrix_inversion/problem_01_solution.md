## Question

Exercise 1. Definition of the Inverse
For:
A = [2 1; 1 1], B = [1 -1; -1 2]
check, without using a formula, whether B = A^-1. Compute AB and BA and relate the result to the definition of the inverse.

## Solution

1. **Computing AB:**
* Multiplying matrix A by matrix B:
AB = [2 1; 1 1] * [1 -1; -1 2]
AB = [(2 * 1) + (1 * -1), (2 * -1) + (1 * 2); (1 * 1) + (1 * -1), (1 * -1) + (1 * 2)]
AB = [2 - 1, -2 + 2; 1 - 1, -1 + 2]
AB = [1 0; 0 1]


2. **Computing BA:**
* Multiplying matrix B by matrix A:
BA = [1 -1; -1 2] * [2 1; 1 1]
BA = [(1 * 2) + (-1 * 1), (1 * 1) + (-1 * 1); (-1 * 2) + (2 * 1), (-1 * 1) + (2 * 1)]
BA = [2 - 1, 1 - 1; -2 + 2, -1 + 2]
BA = [1 0; 0 1]


3. **Relating the Result to the Definition of the Inverse:**
* **Definition:** By definition, a square matrix $B$ is the inverse of matrix $A$ (denoted $A^{-1}$) if and only if their product in both directions equals the identity matrix ($AB = BA = I$).
* **Conclusion:** Because both $AB$ and $BA$ yield the 2 × 2 identity matrix $I = [1 0; 0 1]$, we have confirmed without using any inverse formula that **$B = A^{-1}$**.
