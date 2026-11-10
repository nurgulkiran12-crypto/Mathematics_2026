## Question

Exercise 6. A System with a Parameter — Which Cases Actually Occur?
Analyze, depending on the parameter $a$, the system:


$$\begin{cases} x + y = 2 \\ ax + ay = 4 \end{cases}$$


Among the three possibilities — exactly one solution, infinitely many solutions, no solution — determine which actually occur and for which values of $a$. If one type cannot occur, explain why.

## Solution

1. **Setting Up the Augmented Matrix:**
* We write the linear system as an augmented matrix $[A \mid b]$:

$$\begin{pmatrix} 1 & 1 & \big\vert{} & 2 \\ a & a & \big\vert{} & 4 \end{pmatrix}$$




2. **Applying Gaussian Elimination:**
* Eliminate the entry in the second row, first column by subtracting $a$ times the first row ($R_2 \leftarrow R_2 - aR_1$):
* New row 2: $[a - a(1), \ a - a(1) \mid 4 - a(2)] = [0, \ 0 \mid 4 - 2a]$


* The augmented matrix becomes:

$$\begin{pmatrix} 1 & 1 & \big\vert{} & 2 \\ 0 & 0 & \big\vert{} & 4 - 2a \end{pmatrix}$$




3. **Analyzing the Cases Based on the Parameter $a$:**
* **Case 1: Infinitely Many Solutions ($a = 2$)**
* If we substitute $a = 2$ into the right-hand side of the second row, we get $4 - 2(2) = 0$.
* The matrix becomes:

$$\begin{pmatrix} 1 & 1 & \big\vert{} & 2 \\ 0 & 0 & \big\vert{} & 0 \end{pmatrix}$$


* This corresponds to the equation $x + y = 2$ (with $0 = 0$). Letting the free variable $y = t$, we get the parametric solution:
* $x = 2 - t$
* $y = t$


* Thus, for **$a = 2$**, the system has **infinitely many solutions**.


* **Case 2: No Solution ($a \neq 2$)**
* If $a \neq 2$, then $4 - 2a \neq 0$. The second row translates to:

$$0x + 0y = 4 - 2a \implies 0 = \text{non-zero constant}$$


* This is a mathematical contradiction, meaning the system is inconsistent. Therefore, for **all $a \neq 2$**, the system has **no solution**.


* **Case 3: Exactly One Solution (Does Not Occur)**
* Notice that the determinant of the coefficient matrix is $\det(A) = (1 \cdot a) - (1 \cdot a) = 0$ for **any** real number $a$.
* Because the coefficient matrix is singular (rank 1) for all values of $a$, the lines are never independent enough to intersect at a single unique point. Consequently, the case of **exactly one solution cannot occur**.




4. **Geometric Interpretation:**
* Rearranging both equations into slope-intercept form ($y = -x + 2$ and $y = -x + \frac{4}{a}$ for $a \neq 0$):
* Both equations represent lines with the **exact same slope ($-1$)**.
* When $a = 2$, the second equation becomes $2x + 2y = 4$, which is the exact same line as the first equation (**identical lines $\rightarrow$ infinite intersections**).
* When $a \neq 2$, the y-intercepts differ, meaning the lines are strictly **parallel and distinct $\rightarrow$ no intersections**).
