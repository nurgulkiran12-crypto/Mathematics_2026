## Question

Exercise 12. Homogeneous System
Solve:

$$\begin{cases} x + 2y - z = 0 \\ 2x + 4y - 2z = 0 \\ x - y + 2z = 0 \end{cases}$$

Give all solutions in parametric form and explain why $(0, 0, 0)$ always satisfies a homogeneous system.

## Solution

### 1. Setting Up the Augmented Matrix

We write the homogeneous system as an augmented matrix $[A \mid 0]$:

$$\begin{pmatrix} 1 & 2 & -1 & \mid & 0 \\ 2 & 4 & -2 & \mid & 0 \\ 1 & -1 & 2 & \mid & 0 \end{pmatrix}$$

### 2. Applying Gaussian Elimination

**Step 1:** Eliminate the entry in the second row, first column by subtracting $2$ times the first row ($R_2 \leftarrow R_2 - 2R_1$):

* New row 2: $[2 - 2(1), \ 4 - 2(2), \ -2 - 2(-1) \mid 0 - 0] = [0, \ 0, \ 0 \mid 0]$

**Step 2:** Eliminate the entry in the third row, first column by subtracting the first row ($R_3 \leftarrow R_3 - R_1$):

* New row 3: $[1 - 1, \ -1 - 2, \ 2 - (-1) \mid 0 - 0] = [0, \ -3, \ 3 \mid 0]$

The augmented matrix becomes:

$$\begin{pmatrix} 1 & 2 & -1 & \mid & 0 \\ 0 & 0 & 0 & \mid & 0 \\ 0 & -3 & 3 & \mid & 0 \end{pmatrix}$$

**Step 3:** Swap rows 2 and 3 ($R_2 \leftrightarrow R_3$) to place the non-zero row in the second position:

$$\begin{pmatrix} 1 & 2 & -1 & \mid & 0 \\ 0 & -3 & 3 & \mid & 0 \\ 0 & 0 & 0 & \mid & 0 \end{pmatrix}$$

**Step 4:** Scale the second row by $-\frac{1}{3}$ ($R_2 \leftarrow -\frac{1}{3}R_2$):

$$\begin{pmatrix} 1 & 2 & -1 & \mid & 0 \\ 0 & 1 & -1 & \mid & 0 \\ 0 & 0 & 0 & \mid & 0 \end{pmatrix}$$

### 3. Writing the Solution in Parametric Form

Translate the non-zero rows back into equations:

* **Row 2:** $y - z = 0 \implies y = z$
* **Row 1:** $x + 2y - z = 0$

Since column 3 has no pivot, **$z$ is a free variable**. Let **$z = t$**, where $t \in \mathbb{R}$ is any real parameter.

* From Row 2: **$y = t$**
* Substitute $y = t$ and $z = t$ into Row 1:

$$x + 2(t) - t = 0 \implies x + t = 0 \implies x = -t$$

**Parametric Solution:**

$$\begin{cases} x = -t \\ y = t \\ z = t \end{cases}$$

In vector notation, all solutions are given by $(x, y, z) = t(-1, 1, 1)$ for $t \in \mathbb{R}$, representing a line passing through the origin in $\mathbb{R}^3$.

### 4. Why $(0, 0, 0)$ Always Satisfies a Homogeneous System

A homogeneous linear system has all constant terms on the right-hand side equal to zero ($Ax = 0$). When we substitute $(x, y, z) = (0, 0, 0)$ into any linear equation of the form $a_1x + a_2y + a_3z = 0$, every term becomes zero:

$$
a_1(0) + a_2(0) + a_3(0) = 0 + 0 + 0 = 0
$$
