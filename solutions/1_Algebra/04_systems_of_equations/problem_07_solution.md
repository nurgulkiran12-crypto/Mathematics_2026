## Question

Exercise 7. Choosing a Method Deliberately
Do not solve all of the following systems completely. For each situation, choose the method that best uses its structure and justify your choice:

1. One system with a triangular coefficient matrix:

$$\begin{cases} 2x - y = 3 \\ 4y = 8 \end{cases}$$


2. Three systems $Ax = b_i$ with the same invertible matrix $A$, when $A^{-1}$ is already known.
3. One $3 \times 3$ system for which the inverse matrix is not given and the goal is only to find one solution vector.

For case 1, carry out the chosen method completely. For cases 2 and 3, describe the plan and indicate which part of the computation would be reusable or unnecessary. Do not judge a method by its name alone — refer to the number of right-hand sides and the structure of the matrix.

## Solution

1. **Case 1: Triangular Coefficient Matrix**
* **Chosen Method:** **Back-substitution**. Because the matrix is already upper triangular, elimination is completely bypassed.
* **Complete Solution:**
* From the second equation ($4y = 8$):

$$y = \frac{8}{4} = 2$$


* Substitute $y = 2$ back into the first equation ($2x - y = 3$):

$$2x - 2 = 3 \implies 2x = 5 \implies x = \frac{5}{2} = 2.5$$


* **Solution:** $x = 2.5$, $y = 2$ (or $[2.5;\ 2]$).




2. **Case 2: Multiple Systems with a Known Inverse ($A^{-1}$)**
* **Chosen Method:** **Matrix-vector multiplication ($x_i = A^{-1}b_i$)**.
* **Plan & Reusability:**
* Because $A^{-1}$ is already pre-computed, we do not need to perform Gaussian elimination or find an inverse from scratch for any of the vectors.
* We simply multiply the pre-calculated inverse $A^{-1}$ by each of the three right-hand side vectors independently: $x_1 = A^{-1}b_1$, $x_2 = A^{-1}b_2$, and $x_3 = A^{-1}b_3$.
* **Unnecessary Work:** Re-running row operations or finding $A^{-1}$ three times is completely unnecessary; the heavy computational lifting (finding $A^{-1}$) has already been done and is fully reusable across all three systems.




3. **Case 3: Single $3 \times 3$ System Without an Inverse**
* **Chosen Method:** **Gaussian elimination on the augmented matrix $[A \mid b]$**.
* **Plan & Reusability:**
* Form the augmented matrix $[A \mid b]$, reduce it to row-echelon form via elementary row operations, and solve using back-substitution.
* **Unnecessary Work:** Computing the full matrix inverse $A^{-1}$ (or even computing $\det(A)$ separately) is **completely unnecessary**. Finding $A^{-1}$ requires $n^3$ operations and inverts the entire matrix when we only care about a single target vector $b$. Gaussian elimination targets the specific right-hand side directly and uses far fewer computational steps.
