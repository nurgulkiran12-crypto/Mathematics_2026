## Question

Exercise 13. Does Every Equation Add New Information?
Consider the system:


$$\begin{cases} x_1 + x_2 = 10 \\ x_2 + x_3 = 8 \\ x_1 - x_3 = 2 \end{cases}$$


Solve it and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.
*(Why this exercise: explores linear dependence, redundancy in linear systems, and how rank relates to the amount of independent information present.)*

## Solution

1. **Setting Up the Augmented Matrix:**
* Write the system as an augmented matrix $[A \mid b]$:

$$\begin{pmatrix} 1 & 1 & 0 & \big\vert{} & 10 \\ 0 & 1 & 1 & \big\vert{} & 8 \\ 1 & 0 & -1 & \big\vert{} & 2 \end{pmatrix}$$




2. **Applying Gaussian Elimination:**
* **Step 1:** Eliminate the leading entry in the third row by subtracting row 1 from row 3 ($R_3 \leftarrow R_3 - R_1$):
* New row 3: $[1 - 1, \ 0 - 1, \ -1 - 0 \mid 2 - 10] = [0, \ -1, \ -1 \mid -8]$
* The augmented matrix becomes:

$$\begin{pmatrix} 1 & 1 & 0 & \big\vert{} & 10 \\ 0 & 1 & 1 & \big\vert{} & 8 \\ 0 & -1 & -1 & \big\vert{} & -8 \end{pmatrix}$$




* **Step 2:** Eliminate the entry in the third row, second column by adding row 2 to row 3 ($R_3 \leftarrow R_3 + R_2$):
* New row 3: $[0 + 0, \ -1 + 1, \ -1 + 1 \mid -8 + 8] = [0, \ 0, \ 0 \mid 0]$
* Final row-echelon matrix:

$$\begin{pmatrix} 1 & 1 & 0 & \big\vert{} & 10 \\ 0 & 1 & 1 & \big\vert{} & 8 \\ 0 & 0 & 0 & \big\vert{} & 0 \end{pmatrix}$$






3. **Solving the System in Parametric Form:**
* The appearance of a full row of zeros indicates that the system has infinitely many solutions and one free variable. Translating the non-zero rows back into equations:
* Row 2: $x_2 + x_3 = 8 \implies x_2 = 8 - x_3$
* Row 1: $x_1 + x_2 = 10 \implies x_1 + (8 - x_3) = 10 \implies x_1 = 2 + x_3$


* Let the free variable **$x_3 = t$**, where $t$ is any real number.
* **Parametric Solution:**
* $x_1 = 2 + t$
* $x_2 = 8 - t$
* $x_3 = t$




4. **Checking Equation Independence (Redundancy):**
* Are all three equations independently necessary? **No.** The third equation is completely redundant because it can be derived algebraically from the first two.
* **Proof by Calculation:** Take Equation (1) and subtract Equation (2) from it:

$$(x_1 + x_2) - (x_2 + x_3) = 10 - 8$$


$$x_1 + x_2 - x_2 - x_3 = 2 \implies x_1 - x_3 = 2$$


* This algebraic combination yields **Equation (3)** exactly.
* **Conclusion:** Because the third equation is just a linear combination of the first two equations, it carries no new geometric or algebraic information. The solution set is fully determined by any two of the equations, which corresponds to the row of zeros we found during Gaussian elimination.
