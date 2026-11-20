## Question

Exercise 8. Two Systems with the Same Coefficient Matrix
Solve by elimination the two systems:

1. System 1:

$$
\begin{cases}
2x + y = 5 \\
x - y = 1
\end{cases}
$$

2. System 2:

$$
\begin{cases}
2x + y = 1 \\
x - y = 4
\end{cases}
$$

Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?

## Solution

### 1. Solving System 1

**Augmented matrix $[A \mid b_1]$:**

$$
\begin{pmatrix}
2 & 1 & \mid & 5 \\
1 & -1 & \mid & 1
\end{pmatrix}
$$

**Step 1:** Swap rows 1 and 2 ($R_1 \leftrightarrow R_2$) to place a clean pivot ($1$) in the top-left position:

$$
\begin{pmatrix}
1 & -1 & \mid & 1 \\
2 & 1 & \mid & 5
\end{pmatrix}
$$

**Step 2:** Eliminate the entry below the first pivot by subtracting $2$ times the first row from the second row ($R_2 \leftarrow R_2 - 2R_1$):

* New row 2: $[2 - 2(1), \ 1 - 2(-1) \mid 5 - 2(1)] = [0, \ 3 \mid 3]$

$$
\begin{pmatrix}
1 & -1 & \mid & 1 \\
0 & 3 & \mid & 3
\end{pmatrix}
$$

**Step 3:** Scale the second row by $\frac{1}{3}$ ($R_2 \leftarrow \frac{1}{3}R_2$):

$$
\begin{pmatrix}
1 & -1 & \mid & 1 \\
0 & 1 & \mid & 1
\end{pmatrix}
$$

**Step 4:** Back-substitution:

* From Row 2: **$y = 1$**
* From Row 1 ($x - y = 1$):

$$
x - 1 = 1 \implies x = 2
$$

**Solution 1:** $x = 2$, $y = 1$, or in vector form:

$$
\begin{pmatrix}
2 \\
1
\end{pmatrix}
$$

### 2. Solving System 2

**Augmented matrix $[A \mid b_2]$:**

$$
\begin{pmatrix}
2 & 1 & \mid & 1 \\
1 & -1 & \mid & 4
\end{pmatrix}
$$

**Step 1:** Swap rows 1 and 2 ($R_1 \leftrightarrow R_2$):

$$
\begin{pmatrix}
1 & -1 & \mid & 4 \\
2 & 1 & \mid & 1
\end{pmatrix}
$$

**Step 2:** Apply the exact same row operation ($R_2 \leftarrow R_2 - 2R_1$):

* New row 2: $[2 - 2(1), \ 1 - 2(-1) \mid 1 - 2(4)] = [0, \ 3 \mid -7]$

$$
\begin{pmatrix}
1 & -1 & \mid & 4 \\
0 & 3 & \mid & -7
\end{pmatrix}
$$

**Step 3:** Scale the second row by $\frac{1}{3}$ ($R_2 \leftarrow \frac{1}{3}R_2$):

$$
\begin{pmatrix}
1 & -1 & \mid & 4 \\
0 & 1 & \mid & -\frac{7}{3}
\end{pmatrix}
$$

**Step 4:** Back-substitution:

* From Row 2: **$y = -\frac{7}{3}$**
* From Row 1 ($x - y = 4$):

$$
x - \left(-\frac{7}{3}\right) = 4 \implies x + \frac{7}{3} = \frac{12}{3} \implies x = \frac{5}{3}
$$

**Solution 2:** $x = \frac{5}{3}$, $y = -\frac{7}{3}$, or in vector form:

$$
\begin{pmatrix}
\frac{5}{3} \\
-\frac{7}{3}
\end{pmatrix}
$$

### 3. Comparison of Elimination Steps

* **Identical calculations:** The entire sequence of elementary row operations applied to the **left side** (the coefficient matrix $A$) is completely identical in both systems. The row swap ($R_1 \leftrightarrow R_2$), the elimination step ($R_2 \leftarrow R_2 - 2R_1$), and the scaling factor ($R_2 \leftarrow \frac{1}{3}R_2$) did not change at all, producing the exact same upper-triangular coefficient matrix on the left.
* **Where they differed:** Only the right-hand side column (carrying $b_1$ versus $b_2$) differed, resulting in different intermediate constants and distinct final solution vectors.

### 4. Why This Happens

Elementary row operations are determined strictly by the entries of the coefficient matrix $A$ on the left-hand side of the equations. Because both systems share the exact same coefficient matrix $A$, the structural transformations required to eliminate variables and isolate pivots are identical. This explains why multiple systems with the same matrix $A$ can be solved simultaneously using a single combined augmented matrix $[A \mid b_1 \mid b_2]$.
