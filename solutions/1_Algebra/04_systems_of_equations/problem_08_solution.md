## Question

Exercise 8. Two Systems with the Same Coefficient Matrix
Solve by elimination the two systems:

1. $\begin{cases} 2x + y = 5 \\ x - y = 1 \end{cases}$
2. $\begin{cases} 2x + y = 1 \\ x - y = 4 \end{cases}$

Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?
*(Why this exercise: illustrates that when multiple systems share the same coefficient matrix, the row operations on the left side are identical, previewing the efficiency of matrix inverses and LU decomposition.)*

## Solution

1. **Solving System 1:**
* **Augmented matrix $[A \mid b_1]$:**

$$\begin{pmatrix} 2 & 1 & \big\vert{} & 5 \\ 1 & -1 & \big\vert{} & 1 \end{pmatrix}$$


* **Step 1:** Swap rows 1 and 2 ($R_1 \leftrightarrow R_2$) to place a clean pivot ($1$) in the top-left position:

$$\begin{pmatrix} 1 & -1 & \big\vert{} & 1 \\ 2 & 1 & \big\vert{} & 5 \end{pmatrix}$$


* **Step 2:** Eliminate the entry below the first pivot by subtracting 2 times the first row from the second row ($R_2 \leftarrow R_2 - 2R_1$):
* New row 2: $[2 - 2(1), \ 1 - 2(-1) \mid 5 - 2(1)] = [0, \ 3 \mid 3]$

$$\begin{pmatrix} 1 & -1 & \big\vert{} & 1 \\ 0 & 3 & \big\vert{} & 3 \end{pmatrix}$$




* **Step 3:** Scale the second row by $\frac{1}{3}$ ($R_2 \leftarrow \frac{1}{3}R_2$):

$$\begin{pmatrix} 1 & -1 & \big\vert{} & 1 \\ 0 & 1 & \big\vert{} & 1 \end{pmatrix}$$


* **Step 4:** Back-substitution:
* From Row 2: **$y = 1$**
* From Row 1 ($x - y = 1$): $x - 1 = 1 \implies$ **$x = 2$**


* **Solution 1:** $x = 2, y = 1$ (or $[2;\ 1]$).


2. **Solving System 2:**
* **Augmented matrix $[A \mid b_2]$:**

$$\begin{pmatrix} 2 & 1 & \big\vert{} & 1 \\ 1 & -1 & \big\vert{} & 4 \end{pmatrix}$$


* **Step 1:** Swap rows 1 and 2 ($R_1 \leftrightarrow R_2$):

$$\begin{pmatrix} 1 & -1 & \big\vert{} & 4 \\ 2 & 1 & \big\vert{} & 1 \end{pmatrix}$$


* **Step 2:** Apply the exact same row operation ($R_2 \leftarrow R_2 - 2R_1$):
* New row 2: $[2 - 2(1), \ 1 - 2(-1) \big\vert{} 1 - 2(4)] = [0, \ 3 \mid -7]$

$$\begin{pmatrix} 1 & -1 & \big\vert{} & 4 \\ 0 & 3 & \big\vert{} & -7 \end{pmatrix}$$




* **Step 3:** Scale the second row by $\frac{1}{3}$ ($R_2 \leftarrow \frac{1}{3}R_2$):

$$\begin{pmatrix} 1 & -1 & \big\vert{} & 4 \\ 0 & 1 & \big\vert{} & -7/3 \end{pmatrix}$$


* **Step 4:** Back-substitution:
* From Row 2: **$y = -7/3$**
* From Row 1 ($x - y = 4$): $x - (-7/3) = 4 \implies x + \frac{7}{3} = \frac{12}{3} \implies$ **$x = 5/3$**


* **Solution 2:** $x = 5/3, y = -7/3$ (or $[5/3;\ -7/3]$).


3. **Comparison of Elimination Steps:**
* **Identical calculations:** The entire sequence of row operations applied to the **left side** (the coefficient matrix $A$) is completely identical in both systems. The row swaps, row subtractions, and scaling factors required to reach row-echelon form did not change at all.
* **Where they differed:** Only the right-hand side vector column (carrying $b_1 = [5;\ 1]$ versus $b_2 = [1;\ 4]$) differed, resulting in different constants during the elimination steps and distinct final solution values.


4. **Why This Happens:**
* Elementary row operations depend strictly on the coefficients of the variables on the left-hand side of the equations. Because both systems share the exact same coefficient matrix $A$, the structural transformations needed to isolate the variables are identical.
* This core principle explains why we can solve multiple systems with the same matrix simultaneously (by augmenting $A$ with multiple columns, $[A \mid b_1 \mid b_2]$) or pre-compute $A^{-1}$ once to solve any number of right-hand side vectors efficiently.
