## Question

Exercise 1. From a System to a Matrix
Write the system:
2x - y + z = 4
x + 3y - 2z = 1
3x + y + z = 7
in the form Ax = b. Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.
*(Why this exercise: transitions from linear equations to matrix algebra, laying the foundation for matrix equations and system solvers.)*

## Solution

1. **Writing the System in Matrix Form ($Ax = b$):**
* The linear system can be compactly expressed as the matrix equation:
[2 -1  1] [x]   [4]
[1  3 -2] [y] = [1]
[3  1  1] [z]   [7]


2. **Identifying the Components:**
* **Coefficient matrix A:**
A = [2 -1  1; 1  3 -2; 3  1  1]
* **Vector of unknowns x:**
x = [x; y; z]
* **Right-hand side vector b:**
b = [4; 1; 7]


3. **Explaining Row-to-Equation Correspondence:**
* Matrix multiplication relies on taking the dot product of each row of the coefficient matrix $A$ with the column vector of unknowns $x$:
* **Row 1:** (2 * x) + (-1 * y) + (1 * z) = 4, which matches the first equation: $2x - y + z = 4$.
* **Row 2:** (1 * x) + (3 * y) + (-2 * z) = 1, which matches the second equation: $x + 3y - 2z = 1$.
* **Row 3:** (3 * x) + (1 * y) + (1 * z) = 7, which matches the third equation: $3x + y + z = 7$.


* **Conclusion:** Each row of matrix $A$ holds the exact coefficients for one linear equation, and multiplying $A$ by $x$ reconstructs the original system of equations as a single vector equality.
