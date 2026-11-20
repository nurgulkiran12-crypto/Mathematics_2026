## Question

Exercise 7. Choosing a Method Deliberately
Do not solve all of the following systems completely. For each situation, choose the method that best uses its structure and justify your choice:

1. One system with a triangular coefficient matrix:

$$
\begin{cases}
2x - y = 3 \\
4y = 8
\end{cases}
$$

2. Three systems $Ax = b_i$ with the same invertible matrix $A$, when $A^{-1}$ is already known.
3. One $3 \times 3$ system for which the inverse matrix is not given and the goal is only to find one solution vector.

For case 1, carry out the chosen method completely. For cases 2 and 3, describe the plan and indicate which part of the computation would be reusable or unnecessary. Do not judge a method by its name alone — refer to the number of right-hand sides and the structure of the matrix.

## Solution

### 1. Case 1: Triangular Coefficient Matrix

**Chosen Method:** **Back-substitution**. Because the coefficient matrix is already upper triangular, forward elimination is completely bypassed.

**Complete Solution:**

From the second equation ($4y = 8$):

$$
y = \frac{8}{4} = 2
$$

Substitute $y = 2$ back into the first equation ($2x - y = 3$):

$$
2x - 2 = 3 \implies 2x = 5 \implies x = \frac{5}{2} = 2.5
$$

**Solution:** $x = 2.5$, $y = 2$, or in vector form:

$$
\begin{pmatrix}
2.5 \\
2
\end{pmatrix}
$$

### 2. Case 2: Multiple Systems with a Known Inverse ($A^{-1}$)

**Chosen Method:** **Direct matrix-vector multiplication ($x_i = A^{-1}b_i$)**.

**Plan & Reusability:**

* Because $A^{-1}$ is already pre-computed, we do not need to perform Gaussian elimination or invert the matrix from scratch for any of the three right-hand side vectors.
* We multiply the pre-calculated inverse $A^{-1}$ by each of the three right-hand side vectors independently:

$$
x_1 = A^{-1}b_1, \quad x_2 = A^{-1}b_2, \quad x_3 = A^{-1}b_3
$$

* **Reusable vs. Unnecessary Work:** The heavy computational step (finding $A^{-1}$) has already been completed and is **fully reusable** across all three right-hand sides. Re-running row reduction three separate times would be **completely unnecessary**.

### 3. Case 3: Single $3 \times 3$ System Without an Inverse

**Chosen Method:** **Gaussian elimination on the augmented matrix $[A \mid b]$ followed by back-substitution**.

**Plan & Reusability:**

* Form the augmented matrix $[A \mid b]$, reduce it to upper triangular (row-echelon) form via elementary row operations, and solve for the unknowns using back-substitution.
* **Reusable vs. Unnecessary Work:** Because there is only **one** right-hand side vector $b$, there are no repeated systems that would benefit from reusing a factorization or inverse. Computing the full matrix inverse $A^{-1}$ is **completely unnecessary**, as inverting a matrix requires significantly more operations than reducing a single augmented column directly.
