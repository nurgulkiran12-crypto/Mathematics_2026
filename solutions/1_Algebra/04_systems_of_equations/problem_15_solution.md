## Question

Exercise 15. Classifying Three Systems
For each of the following systems, perform only as much elimination as necessary to recognize its type:

* **System 1:**
x + y = 2
x - y = 0
* **System 2:**
x + y = 2
2x + 2y = 4
* **System 3:**
x + y = 2
2x + 2y = 5

For each, justify the classification: one solution, infinitely many solutions, or no solution.
*(Why this exercise: demonstrates how minimal elimination or inspecting coefficient-to-constant ratios quickly reveals the structural type of linear systems without full back-substitution.)*

## Solution

1. **System 1 Analysis:**
* **Augmented Matrix:**

$$\begin{pmatrix} 1 & 1 & \big\vert{} & 2 \\ 1 & -1 & \big\vert{} & 0 \end{pmatrix}$$


* **Minimal Elimination ($R_2 \leftarrow R_2 - R_1$):**

$$\begin{pmatrix} 1 & 1 & \big\vert{} & 2 \\ 0 & -2 & \big\vert{} & -2 \end{pmatrix}$$


* **Classification & Justification:** **Exactly one solution**. After one row operation, we obtain two non-zero pivot rows with distinct leading entries, meaning every variable is constrained by a unique pivot. (Solving this gives $y = 1$ and $x = 1$).


2. **System 2 Analysis:**
* **Augmented Matrix:**

$$\begin{pmatrix} 1 & 1 & \big\vert{} & 2 \\ 2 & 2 & \big\vert{} & 4 \end{pmatrix}$$


* **Minimal Elimination ($R_2 \leftarrow R_2 - 2R_1$):**

$$\begin{pmatrix} 1 & 1 & \big\vert{} & 2 \\ 0 & 0 & \big\vert{} & 0 \end{pmatrix}$$


* **Classification & Justification:** **Infinitely many solutions**. The second equation completely eliminates into a trivial identity row ($0 = 0$). This occurs because the second equation is an exact multiple of the first ($2x + 2y = 4$ is just $2(x + y = 2)$), meaning both equations describe the exact same geometric line in the plane.


3. **System 3 Analysis:**
* **Augmented Matrix:**

$$\begin{pmatrix} 1 & 1 & \big\vert{} & 2 \\ 2 & 2 & \big\vert{} & 5 \end{pmatrix}$$


* **Minimal Elimination ($R_2 \leftarrow R_2 - 2R_1$):**

$$\begin{pmatrix} 1 & 1 & \big\vert{} & 2 \\ 0 & 0 & \big\vert{} & 1 \end{pmatrix}$$


* **Classification & Justification:** **No solution (inconsistent)**. The elimination step yields a mathematical contradiction in the second row ($0x + 0y = 1 \implies 0 = 1$). Geometrically, the left-hand sides are proportional (giving parallel lines with the same slope), but their right-hand constants do not scale proportionally ($2 \times 2 \neq 5$), meaning the lines are distinct and never intersect.
