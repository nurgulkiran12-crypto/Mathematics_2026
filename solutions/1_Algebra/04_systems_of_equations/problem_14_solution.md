## Question

Exercise 14. A Small Change in the Right-Hand Side
Compare the systems:

1. System 1:

$$
\begin{cases}
x + y = 2 \\
2x - y = 1 \\
3x = 3
\end{cases}
$$

2. System 2:

$$
\begin{cases}
x + y = 2 \\
2x - y = 1 \\
3x = 3.1
\end{cases}
$$

Check the consistency of each system and explain why a small change in one number can change the type of the system.

## Solution

### 1. Consistency of System 1

First, solve the first two equations to find where they intersect:

$$
\begin{cases}
x + y = 2 \\
2x - y = 1
\end{cases}
$$

Adding the two equations eliminates $y$:

$$
(x + y) + (2x - y) = 2 + 1 \implies 3x = 3 \implies x = 1
$$

Substitute $x = 1$ into $x + y = 2$:

$$
1 + y = 2 \implies y = 1
$$

Now check the third equation ($3x = 3$) at $x = 1$:

$$
3(1) = 3
$$

The third equation holds without contradiction. Therefore, **System 1 is consistent** and has **one unique solution**: $(x, y) = (1, 1)$.

### 2. Consistency of System 2

The first two equations remain unchanged, so their unique intersection is still $(x, y) = (1, 1)$, which requires $x = 1$.

Now check the third equation ($3x = 3.1$) at $x = 1$:

$$
3(1) = 3 \neq 3.1
$$

In augmented matrix form for System 2:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & -1 & \mid & 1 \\
3 & 0 & \mid & 3.1
\end{pmatrix}
$$

Eliminating the first two equations yields $x = 1$, and substituting into the third row gives $0 = 0.1$, a contradiction. Therefore, **System 2 is inconsistent** and has **no solution**.

### 3. Why a Small Change Can Change the System Type

An overdetermined system (three equations with only two unknowns $x$ and $y$) has a solution **only if** all three lines pass through the **exact same point**.

* In **System 1**, the third line ($x = 1$) passes right through the intersection $(1, 1)$ of the first two lines, so all three share a common point.
* Changing the right-hand side slightly from $3$ to $3.1$ shifts the third line from $x = 1$ to $x = \frac{3.1}{3} \approx 1.033$. Even a tiny shift moves the line off the point $(1, 1)$, so no single point satisfies all three equations at once.

Geometrically, this illustrates **ill-conditioning / sensitivity to perturbation** in overdetermined systems: a small change in the data moves the constraints out of alignment and switches the system from **consistent (unique solution)** to **inconsistent (no solution)**.
