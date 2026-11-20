## Question

Exercise 10. A Polynomial Through Three Points
Find a polynomial $p(x) = ax^2 + bx + c$ whose graph passes through $(0, 1)$, $(1, 3)$, and $(2, 9)$. Reduce the problem to a system of equations and check the result by substituting all three points.

## Solution

### 1. Setting Up the System of Equations

Substitute each given point $(x, p(x))$ into $p(x) = ax^2 + bx + c$:

* For $(0, 1)$:

$$
a(0)^2 + b(0) + c = 1 \implies c = 1
$$

* For $(1, 3)$:

$$
a(1)^2 + b(1) + c = 3 \implies a + b + c = 3
$$

* For $(2, 9)$:

$$
a(2)^2 + b(2) + c = 9 \implies 4a + 2b + c = 9
$$

### 2. Reducing to a Linear System and Matrix Form

Substituting $c = 1$ into the second and third equations gives:

$$
\begin{cases}
a + b + 1 = 3 \\
4a + 2b + 1 = 9
\end{cases}
$$

Simplifying the constant terms yields the $2 \times 2$ linear system:

$$
\begin{cases}
a + b = 2 \\
4a + 2b = 8
\end{cases}
$$

In augmented matrix form for $(a, b)$ after setting $c = 1$:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
4 & 2 & \mid & 8
\end{pmatrix}
$$

### 3. Solving the System

From $(0, 1)$, we already have **$c = 1$**.

From $a + b = 2$, express $b$ in terms of $a$:

$$
b = 2 - a
$$

Substitute $b = 2 - a$ into $4a + 2b = 8$:

$$
4a + 2(2 - a) = 8
$$

$$
4a + 4 - 2a = 8
$$

$$
2a + 4 = 8 \implies 2a = 4 \implies a = 2
$$

Now substitute $a = 2$ back into $b = 2 - a$:

$$
b = 2 - 2 = 0
$$

With $a = 2$, $b = 0$, and $c = 1$, the resulting polynomial is:

$$
p(x) = 2x^2 + 1
$$

### 4. Checking All Three Points

Substitute $x = 0$, $x = 1$, and $x = 2$ into $p(x) = 2x^2 + 1$:

* **Point $(0, 1)$:**

$$
p(0) = 2(0)^2 + 1 = 1
$$

* **Point $(1, 3)$:**

$$
p(1) = 2(1)^2 + 1 = 3
$$

* **Point $(2, 9)$:**

$$
p(2) = 2(2)^2 + 1 = 9
$$

All three points match the required values, so $p(x) = 2x^2 + 1$ is verified.
