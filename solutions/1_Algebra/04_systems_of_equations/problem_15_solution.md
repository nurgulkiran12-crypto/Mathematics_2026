## Question

Exercise 15. Classifying Three Systems
For each of the following systems, perform only as much elimination as necessary to recognize its type:

* **System 1:**

$$
\begin{cases}
x + y = 2 \\
x - y = 0
\end{cases}
$$

* **System 2:**

$$
\begin{cases}
x + y = 2 \\
2x + 2y = 4
\end{cases}
$$

* **System 3:**

$$
\begin{cases}
x + y = 2 \\
2x + 2y = 5
\end{cases}
$$

For each, justify the classification: one solution, infinitely many solutions, or no solution.

## Solution

### 1. System 1

**Augmented Matrix:**

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
1 & -1 & \mid & 0
\end{pmatrix}
$$

**Minimal Elimination:**

Subtract row 1 from row 2 ($R_2 \leftarrow R_2 - R_1$):

* New row 2: $[1 - 1, \ -1 - 1 \mid 0 - 2] = [0, \ -2 \mid -2]$

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & -2 & \mid & -2
\end{pmatrix}
$$

**Classification & Justification:**

* **Type:** **One unique solution** (specifically, $y = 1$ and $x = 1$).
* **Justification:** Both columns have non-zero pivots ($1$ in column 1 and $-2$ in column 2), and there are no contradictory rows. Since the coefficient matrix has full rank ($2$), the two lines have different slopes and intersect at a single unique point.

### 2. System 2

**Augmented Matrix:**

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & 2 & \mid & 4
\end{pmatrix}
$$

**Minimal Elimination:**

Subtract $2$ times row 1 from row 2 ($R_2 \leftarrow R_2 - 2R_1$):

* New row 2: $[2 - 2(1), \ 2 - 2(1) \mid 4 - 2(2)] = [0, \ 0 \mid 0]$

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 0
\end{pmatrix}
$$

**Classification & Justification:**

* **Type:** **Infinitely many solutions** (parametrized by $x = 2 - t$, $y = t$ for $t \in \mathbb{R}$).
* **Justification:** The second row reduces completely to the trivial identity $0 = 0$, meaning the second equation is simply a scalar multiple of the first. With only $1$ pivot for $2$ variables, $y$ is a free variable, and the two equations describe the exact same line.

### 3. System 3

**Augmented Matrix:**

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & 2 & \mid & 5
\end{pmatrix}
$$

**Minimal Elimination:**

Subtract $2$ times row 1 from row 2 ($R_2 \leftarrow R_2 - 2R_1$):

* New row 2: $[2 - 2(1), \ 2 - 2(1) \mid 5 - 2(2)] = [0, \ 0 \mid 1]$

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 1
\end{pmatrix}
$$

**Classification & Justification:**

* **Type:** **No solution** (inconsistent system).
* **Justification:** The second row reduces to $0x + 0y = 1 \implies 0 = 1$, which is a mathematical contradiction. Geometrically, the two equations represent parallel lines with identical slopes ($-1$) but different y-intercepts, so they never intersect.
