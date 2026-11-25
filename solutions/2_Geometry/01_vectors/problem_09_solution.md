## Question

Exercise 9. Cross Product as a Perpendicular Direction
For $u = (1, 2, 0)$ and $v = (0, 1, 3)$ compute $u \times v$. Use dot products to check perpendicularity to both vectors, compute $v \times u$, and compare the results.

## Solution

### 1. Computing the Cross Product $u \times v$

**Mechanism Used:** 3D vector cross product via cofactor expansion along the first row of the symbolic $3 \times 3$ determinant formed by standard basis vectors $(\mathbf{i}, \mathbf{j}, \mathbf{k})$ and the components of $u = (1, 2, 0)$ and $v = (0, 1, 3)$:

$$
\begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
1 & 2 & 0 \\
0 & 1 & 3
\end{vmatrix}
$$

Expand into $2 \times 2$ minor determinants for each component:

* **$\mathbf{i}$-component:**

$$
\begin{vmatrix}
2 & 0 \\
1 & 3
\end{vmatrix}
= (2)(3) - (0)(1) = 6 - 0 = 6
$$

* **$\mathbf{j}$-component (with alternating minus sign):**

$$
-\begin{vmatrix}
1 & 0 \\
0 & 3
\end{vmatrix}
= -\big((1)(3) - (0)(0)\big) = -(3 - 0) = -3
$$

* **$\mathbf{k}$-component:**

$$
\begin{vmatrix}
1 & 2 \\
0 & 1
\end{vmatrix}
= (1)(1) - (2)(0) = 1 - 0 = 1
$$

Combining all three components gives:

$$
u \times v = (6, -3, 1)
$$

### 2. Checking Perpendicularity Using Dot Products

**Mechanism Used:** Orthogonality criterion ($a \cdot b = 0 \iff a \perp b$). We verify that $(u \times v) \cdot u = 0$ and $(u \times v) \cdot v = 0$.

* **Check against $u = (1, 2, 0)$:**

$$
(u \times v) \cdot u = (6)(1) + (-3)(2) + (1)(0) = 6 - 6 + 0 = 0
$$

* **Check against $v = (0, 1, 3)$:**

$$
(u \times v) \cdot v = (6)(0) + (-3)(1) + (1)(3) = 0 - 3 + 3 = 0
$$

Since both dot products equal $0$, the cross product $u \times v = (6, -3, 1)$ is strictly perpendicular to both $u$ and $v$ (and therefore normal to the plane spanned by $u$ and $v$).

### 3. Computing $v \times u$

**Mechanism Used:** Symbolic determinant expansion with the rows for $v = (0, 1, 3)$ and $u = (1, 2, 0)$ swapped:

$$
\begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
0 & 1 & 3 \\
1 & 2 & 0
\end{vmatrix}
$$

Compute each component from its $2 \times 2$ minor:

* **$\mathbf{i}$-component:** $(1)(0) - (3)(2) = 0 - 6 = -6$
* **$\mathbf{j}$-component:** $-\big((0)(0) - (3)(1)\big) = -(-3) = 3$
* **$\mathbf{k}$-component:** $(0)(2) - (1)(1) = 0 - 1 = -1$

Combining the components gives:

$$
v \times u = (-6, 3, -1)
$$

### 4. Comparing $u \times v$ and $v \times u$ (Algebraic & Geometric Interpretation)

* **Anti-Commutativity ($v \times u = -(u \times v)$):** Comparing $(6, -3, 1)$ and $(-6, 3, -1)$ shows that every component flips sign:

$$
v \times u = (-6, 3, -1) = -(6, -3, 1) = -(u \times v)
$$

* **Geometric Meaning (Right-Hand Rule & Area):** Both vectors share the **exact same length** ($\|u \times v\| = \|v \times u\| = \sqrt{6^2 + (-3)^2 + 1^2} = \sqrt{46}$, which equals the area of the parallelogram spanned by $u$ and $v$) and lie along the **exact same normal line** perpendicular to the plane of $u$ and $v$, but they point in **opposite orientations** ($180^\circ$ apart) in accordance with the right-hand rule.
