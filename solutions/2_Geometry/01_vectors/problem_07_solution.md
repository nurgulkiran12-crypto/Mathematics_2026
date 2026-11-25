## Question

Exercise 7. Linear Dependence Without Heavy Computation
Given:

$$
u = (1, 2, 3), \quad v = (2, 4, 6), \quad w = (0, 1, 1)
$$

Identify a specific relation between $u$ and $v$, decide whether the three vectors can be linearly independent, and explain why no long calculation is needed.

## Solution

### 1. Identifying the Specific Relation Between $u$ and $v$

**Mechanism Used:** Component-wise ratio inspection to detect scalar proportionality ($v = c \cdot u$).

Comparing each coordinate of $v = (2, 4, 6)$ with the corresponding coordinate of $u = (1, 2, 3)$:

$$
\frac{2}{1} = 2, \quad \frac{4}{2} = 2, \quad \frac{6}{3} = 2
$$

Every component of $v$ is exactly twice the corresponding component of $u$, giving the exact linear relation:

$$
v = 2u \quad \text{or equivalently} \quad 2u - v = \mathbf{0}
$$

### 2. Deciding Linear Independence of $\{u, v, w\}$

**Mechanism Used:** Definition of linear dependence—a set of vectors $\{v_1, v_2, \dots, v_k\}$ is **linearly dependent** if there exist scalars $c_1, c_2, \dots, c_k$, not all zero, such that $c_1 v_1 + c_2 v_2 + \dots + c_k v_k = \mathbf{0}$.

Using our relation $2u - v = \mathbf{0}$, we construct a non-trivial linear combination of all three vectors by setting $c_1 = 2$, $c_2 = -1$, and $c_3 = 0$:

$$
2u - 1v + 0w = 2(1, 2, 3) - 1(2, 4, 6) + 0(0, 1, 1) = (0, 0, 0)
$$

Because at least one coefficient is non-zero ($c_1 = 2 \neq 0$, $c_2 = -1 \neq 0$), the three vectors **cannot be linearly independent**—they are **linearly dependent**.

### 3. Verification Check

Verify component-by-component that $2u - v + 0w = (0, 0, 0)$:

* **First coordinate:** $2(1) - 1(2) + 0(0) = 2 - 2 + 0 = 0$
* **Second coordinate:** $2(2) - 1(4) + 0(1) = 4 - 4 + 0 = 0$
* **Third coordinate:** $2(3) - 1(6) + 0(1) = 6 - 6 + 0 = 0$

All three coordinates equal zero, confirming the linear dependence relation.

### 4. Why No Long Calculation Is Needed (Algebraic & Geometric Explanation)

* **Algebraic Shortcut (Subset Rule):** A fundamental theorem of linear algebra states that **if any subset of vectors is linearly dependent, the entire set is automatically linearly dependent**. Since $\{u, v\}$ already exhibits an obvious scalar multiple ($v = 2u$), we do not need to set up a $3 \times 3$ matrix, run Gaussian elimination, or compute a determinant—the third vector $w$ can simply be assigned a weight of $0$.
* **Geometric Interpretation:** Because $v = 2u$, the vectors $u$ and $v$ are **collinear** (they lie along the exact same line through the origin in $\mathbb{R}^3$). Adding a third vector $w$ spans at most a **2D plane** (rather than a full 3D volume), meaning $v$ contributes no new spatial direction.
  
