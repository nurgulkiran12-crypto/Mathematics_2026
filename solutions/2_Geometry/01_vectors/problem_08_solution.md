## Question

Exercise 8. Linear Combination and Checking the Result
Check whether $w = (5, 1)$ can be written as:

$$
w = au + bv
$$

where $u = (1, 1)$ and $v = (2, -1)$. If so, find $a, b$, reconstruct $w$ from them, and explain the geometric meaning of the existence of such coefficients.

## Solution

### 1. Setting Up the Linear System

**Mechanism Used:** Component-wise equivalence of vectors. Writing $w = au + bv$ translates into matching each coordinate of the linear combination with the target vector $w = (5, 1)$:

$$
a(1, 1) + b(2, -1) = (5, 1)
$$

$$
(a + 2b, \ a - b) = (5, 1)
$$

Equating the first and second components yields a $2 \times 2$ system of linear equations:

$$
\begin{cases}
a + 2b = 5 \\
a - b = 1
\end{cases}
$$

In augmented matrix form $[A \mid w]$:

$$
\begin{pmatrix}
1 & 2 & \mid & 5 \\
1 & -1 & \mid & 1
\end{pmatrix}
$$

### 2. Solving for the Coefficients $a$ and $b$

**Mechanism Used:** Gaussian elimination (row subtraction) followed by back-substitution.

**Step 1:** Eliminate $a$ in the second row by subtracting row 1 from row 2 ($R_2 \leftarrow R_2 - R_1$):

* New row 2: $[1 - 1, \ -1 - 2 \mid 1 - 5] = [0, \ -3 \mid -4]$

$$
\begin{pmatrix}
1 & 2 & \mid & 5 \\
0 & -3 & \mid & -4
\end{pmatrix}
$$

**Step 2:** Solve the second row for $b$:

$$
-3b = -4 \implies b = \frac{-4}{-3} = \frac{4}{3}
$$

**Step 3:** Substitute $b = \frac{4}{3}$ back into the first equation ($a + 2b = 5$) to find $a$:

$$
a + 2\left(\frac{4}{3}\right) = 5 \implies a + \frac{8}{3} = \frac{15}{3}
$$

$$
a = \frac{15}{3} - \frac{8}{3} = \frac{7}{3}
$$

Thus, **$w$ can be written as a linear combination of $u$ and $v$** with unique coefficients **$a = \frac{7}{3}$** and **$b = \frac{4}{3}$**.

### 3. Reconstructing $w$ (Verification Check)

Substitute $a = \frac{7}{3}$ and $b = \frac{4}{3}$ back into $au + bv$:

$$
\frac{7}{3}(1, 1) + \frac{4}{3}(2, -1) = \left(\frac{7}{3}, \frac{7}{3}\right) + \left(\frac{8}{3}, -\frac{4}{3}\right)
$$

Combine the fractions component-wise:

$$
\left(\frac{7 + 8}{3}, \ \frac{7 - 4}{3}\right) = \left(\frac{15}{3}, \ \frac{3}{3}\right) = (5, 1) = w
$$

The reconstruction reproduces $w = (5, 1)$ identically, verifying that $a = \frac{7}{3}$ and $b = \frac{4}{3}$ are exact.

### 4. Geometric Meaning of the Existence of $a$ and $b$

* **Spanning the 2D Plane ($\mathbb{R}^2$):** Because $u = (1, 1)$ and $v = (2, -1)$ do not lie on the same line (neither is a scalar multiple of the other), they are linearly independent and form a **basis** for the entire 2D plane $\mathbb{R}^2$. Therefore, any target vector $w$ in the plane lies inside $\mathrm{span}\{u, v\}$.
* **Oblique Coordinate Grid (Parallelogram Navigation):** Geometrically, finding $a = \frac{7}{3}$ and $b = \frac{4}{3}$ means you can reach the point $(5, 1)$ starting from the origin $(0, 0)$ by moving $\frac{7}{3}$ units along the tilted axis defined by $u$ and then $\frac{4}{3}$ units parallel to the tilted axis defined by $v$ (forming the diagonal of a scaled parallelogram).
