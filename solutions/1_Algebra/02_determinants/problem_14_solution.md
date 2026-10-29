## Question

Exercise 14. A System of Equations and the Determinant
Consider the system Ax = b, where:
A = [1 2; k 4]
For which values of k does the system have exactly one solution for every b? For the remaining value, give an example of a right-hand side b for which the system has infinitely many solutions, and an example for which it has no solution.

## Solution

1. **Finding the Determinant and Unique Solution Condition:**
* For a square 2 × 2 matrix, the system $Ax = b$ has a **unique solution** for every right-hand side vector $b$ if and only if the matrix is invertible, which means its determinant is non-zero ($\det(A) \neq 0$).
* Compute the determinant of $A$:
$\det(A) = (1 \times 4) - (2 \times k) = 4 - 2k$
* Set the determinant not equal to zero:
$4 - 2k \neq 0 \implies 2k \neq 4 \implies k \neq 2$
* Therefore, the system has exactly one solution for every $b$ for all **$k \neq 2$**.


2. **Analyzing the Remaining Value ($k = 2$):**
* When $k = 2$, the matrix becomes:
A = [1 2; 2 4]
* Notice that the second row is an exact multiple of the first row ($R_2 = 2R_1$), meaning $\det(A) = 0$ and the matrix is singular.
* Writing out the augmented matrix $[A \mid b]$ for $b = [b_1; b_2]$:
[1 2 | b1; 2 4 | b2]
* Performing elimination ($R_2 \leftarrow R_2 - 2R_1$):
[1 2 | b1; 0 0 | b2 - 2b_1]
* For the system to be consistent (have solutions), we must have $b_2 - 2b_1 = 0$, or **$b_2 = 2b_1$**.


3. **Example of Infinitely Many Solutions:**
* To get infinitely many solutions, we choose a vector $b$ that satisfies the consistency condition $b_2 = 2b_1$.
* Let **$b = [1; 2]$** (since $2 = 2 \times 1$).
* The augmented matrix becomes:
[1 2 | 1; 0 0 | 0]
* This yields the single equation $x_1 + 2x_2 = 1$, giving a free variable and **infinitely many solutions** (e.g., setting $x_2 = t$, we get $x_1 = 1 - 2t$).


4. **Example of No Solution:**
* To get no solution, we choose a vector $b$ that violates the consistency condition ($b_2 \neq 2b_1$).
* Let **$b = [1; 3]$** (since $3 \neq 2 \times 1$).
* The augmented matrix becomes:
[1 2 | 1; 0 0 | 3]
* The second row translates to the impossible equation $0x_1 + 0x_2 = 3$, or $0 = 3$. Because this is a contradiction, the system has **no solution**.
