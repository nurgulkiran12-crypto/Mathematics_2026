## Question

Exercise 13. Does Every Equation Add New Information?
Consider the system:

$$
\begin{cases}
x_1 + x_2 = 10 \\
x_2 + x_3 = 8 \\
x_1 - x_3 = 2
\end{cases}
$$

Solve it and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.

## Solution

### 1. Setting Up the Augmented Matrix

We write the system as an augmented matrix $[A \mid b]$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
1 & 0 & -1 & \mid & 2
\end{pmatrix}
$$

### 2. Applying Gaussian Elimination

**Step 1:** Eliminate the leading entry in row 3 by subtracting row 1 from row 3 ($R_3 \leftarrow R_3 - R_1$):

* New row 3: $[1 - 1, \ 0 - 1, \ -1 - 0 \mid 2 - 10] = [0, \ -1, \ -1 \mid -8]$

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
0 & -1 & -1 & \mid & -8
\end{pmatrix}
$$

**Step 2:** Eliminate the entry in row 3, column 2 by adding row 2 to row 3 ($R_3 \leftarrow R_3 + R_2$):

* New row 3: $[0 + 0, \ -1 + 1, \ -1 + 1 \mid -8 + 8] = [0, \ 0, \ 0 \mid 0]$

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
0 & 0 & 0 & \mid & 0
\end{pmatrix}
$$

### 3. Solving the System in Parametric Form

The third row reduces completely to $0 = 0$, leaving two pivot columns ($x_1$ and $x_2$) and one free variable ($x_3$).

Let **$x_3 = t$**, where $t \in \mathbb{R}$ is any real parameter:

* From Row 2 ($x_2 + x_3 = 8$):

$$
x_2 = 8 - t
$$

* From Row 1 ($x_1 + x_2 = 10$):

$$
x_1 + (8 - t) = 10 \implies x_1 = 2 + t
$$

**Parametric Solution:**

$$
\begin{cases}
x_1 = 2 + t \\
x_2 = 8 - t \\
x_3 = t
\end{cases}
$$

In vector notation, the solution set is $(x_1, x_2, x_3) = (2, 8, 0) + t(1, -1, 1)$ for $t \in \mathbb{R}$, which describes a straight line in $\mathbb{R}^3$.

### 4. Checking Whether All Three Equations Are Necessary

**No**, not all three equations are independently necessary. Because the third row eliminated to $0 = 0$, the third equation adds **no new constraint** to the system—it is completely redundant and follows automatically from the first two equations.

**Proof by Direct Calculation:**

Take **Equation 1** and subtract **Equation 2** from it:

$$
(x_1 + x_2) - (x_2 + x_3) = 10 - 8
$$

Simplifying the left-hand side cancels $x_2$:

$$
x_1 + x_2 - x_2 - x_3 = 2 \implies x_1 - x_3 = 2
$$

This produces **Equation 3** identically. Therefore, the first two equations alone completely determine the exact same solution set.
