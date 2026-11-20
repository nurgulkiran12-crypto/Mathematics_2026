## Question

Exercise 11. A Parameter in a System of Three Equations
Analyze the number of solutions depending on $t$:

$$\begin{cases} x + y + z = 1 \\ x + ty + z = 2 \\ x + y + tz = 3 \end{cases}$$

Use elimination and separately analyze the parameter values for which a standard calculation step ceases to be valid.

## Solution

### 1. Setting Up the Augmented Matrix

We write the linear system as an augmented matrix $[A \mid b]$:

$$\begin{pmatrix} 1 & 1 & 1 & \mid & 1 \\ 1 & t & 1 & \mid & 2 \\ 1 & 1 & t & \mid & 3 \end{pmatrix}$$

### 2. Applying Gaussian Elimination

**Step 1:** Eliminate the leading entry in row 2 by subtracting row 1 from row 2 ($R_2 \leftarrow R_2 - R_1$):

* New row 2: $[1 - 1, \ t - 1, \ 1 - 1 \mid 2 - 1] = [0, \ t - 1, \ 0 \mid 1]$

**Step 2:** Eliminate the leading entry in row 3 by subtracting row 1 from row 3 ($R_3 \leftarrow R_3 - R_1$):

* New row 3: $[1 - 1, \ 1 - 1, \ t - 1 \mid 3 - 1] = [0, \ 0, \ t - 1 \mid 2]$

The augmented matrix simplifies to upper-triangular form:

$$\begin{pmatrix} 1 & 1 & 1 & \mid & 1 \\ 0 & t - 1 & 0 & \mid & 1 \\ 0 & 0 & t - 1 & \mid & 2 \end{pmatrix}$$

### 3. Analyzing Where Standard Calculation Steps Cease to Be Valid

The diagonal pivot entries are $1$, $(t - 1)$, and $(t - 1)$. Standard back-substitution requires dividing by the pivots $(t - 1)$ to solve for $y$ and $z$.

This division **ceases to be valid when $t - 1 = 0 \implies t = 1$**, because division by zero is undefined. Therefore, $t = 1$ must be analyzed separately from all other values of $t$.

### 4. Case-by-Case Analysis Based on $t$

**Case 1: $t = 1$ (Critical Value)**

Substituting $t = 1$ into the upper-triangular matrix gives:

$$\begin{pmatrix} 1 & 1 & 1 & \mid & 1 \\ 0 & 0 & 0 & \mid & 1 \\ 0 & 0 & 0 & \mid & 2 \end{pmatrix}$$

The second row translates to $0x + 0y + 0z = 1 \implies 0 = 1$ (and the third gives $0 = 2$), which is a mathematical contradiction.

Thus, for **$t = 1$**, the system is inconsistent and has **no solution**.

**Case 2: $t \neq 1$ (General Case)**

Since $t \neq 1$, we have $t - 1 \neq 0$, so dividing by $(t - 1)$ is valid. Using back-substitution:

* From Row 3:

$$(t - 1)z = 2 \implies z = \frac{2}{t - 1}$$

* From Row 2:

$$(t - 1)y = 1 \implies y = \frac{1}{t - 1}$$

* From Row 1 ($x + y + z = 1$):

$$x + \frac{1}{t - 1} + \frac{2}{t - 1} = 1 \implies x + \frac{3}{t - 1} = 1$$

$$x = 1 - \frac{3}{t - 1} = \frac{(t - 1) - 3}{t - 1} = \frac{t - 4}{t - 1}$$

Thus, for **all $t \neq 1$**, the system has **exactly one unique solution**:

$$
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix}
=
\begin{pmatrix}
\frac{t - 4}{t - 1} \\
\frac{1}{t - 1} \\
\frac{2}{t - 1}
\end{pmatrix}
