## Question

Exercise 4. Dot Product and Perpendicularity
For $u = (1, 2, -1)$ and $v = (2, -1, 3)$ compute $u \cdot v$ and determine whether the vectors are perpendicular. Then find $a$ so that $w = (2, -1, a)$ is perpendicular to $u$, and check the result.

## Solution

### 1. Computing the Dot Product $u \cdot v$

**Mechanism Used:** Component-wise Euclidean dot product (inner product) in $\mathbb{R}^3$, defined for $u = (u_1, u_2, u_3)$ and $v = (v_1, v_2, v_3)$ as $u \cdot v = u_1 v_1 + u_2 v_2 + u_3 v_3$.

Substituting $u = (1, 2, -1)$ and $v = (2, -1, 3)$:

$$
u \cdot v = (1)(2) + (2)(-1) + (-1)(3)
$$

$$
u \cdot v = 2 - 2 - 3 = -3
$$

### 2. Determining Perpendicularity (Orthogonality)

**Mechanism Used:** Orthogonality criterion via the geometric dot product formula $u \cdot v = \|u\|\|v\|\cos\theta$. Two non-zero vectors are perpendicular ($\theta = 90^\circ$) if and only if $u \cdot v = 0$.

* Because $u \cdot v = -3 \neq 0$, the vectors $u$ and $v$ are **not perpendicular**.
* **Geometric Interpretation:** Since the dot product is strictly negative ($-3 < 0$), $\cos\theta < 0$, which means the angle between $u$ and $v$ is **obtuse** ($90^\circ < \theta < 180^\circ$).

### 3. Finding $a$ So That $w = (2, -1, a)$ Is Perpendicular to $u$

**Mechanism Used:** Enforcing the orthogonality condition $u \cdot w = 0$ and solving the resulting linear equation for the unknown component $a$.

Set the dot product of $u = (1, 2, -1)$ and $w = (2, -1, a)$ equal to zero:

$$
u \cdot w = (1)(2) + (2)(-1) + (-1)(a) = 0
$$

Simplify the terms:

$$
2 - 2 - a = 0 \implies -a = 0 \implies a = 0
$$

Thus, the required value is **$a = 0$**, giving the vector $w = (2, -1, 0)$.

### 4. Checking the Result

Substitute $a = 0$ back into $w = (2, -1, 0)$ and verify both $u \cdot w = 0$ and the Pythagorean theorem for right triangles ($\|u + w\|^2 = \|u\|^2 + \|w\|^2$):

* **Dot Product Check:**

$$
u \cdot w = (1)(2) + (2)(-1) + (-1)(0) = 2 - 2 + 0 = 0
$$

* **Pythagorean Theorem Check:**

$$
\|u\|^2 = 1^2 + 2^2 + (-1)^2 = 6, \quad \|w\|^2 = 2^2 + (-1)^2 + 0^2 = 5
$$

$$
u + w = (3, 1, -1) \implies \|u + w\|^2 = 3^2 + 1^2 + (-1)^2 = 11 = 6 + 5
$$

Both checks confirm that $w = (2, -1, 0)$ meets $u = (1, 2, -1)$ at an exact $90^\circ$ right angle in $\mathbb{R}^3$.
