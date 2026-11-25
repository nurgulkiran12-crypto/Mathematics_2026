## Question

Exercise 12. A Normal Vector to a Plane
Given $A = (1, 0, 2)$, $B = (2, 1, 0)$, and $C = (0, 3, 1)$. Construct two vectors lying in the plane, find a vector perpendicular to both, and check the perpendicularity using dot products.

## Solution

### 1. Constructing Two Vectors Lying in the Plane

**Mechanism Used:** Displacement vector construction (head-minus-tail rule, $\overrightarrow{PQ} = Q - P$) anchored at the shared reference point $A = (1, 0, 2)$. Since $A$, $B$, and $C$ all lie on the plane, the directed segments connecting $A$ to $B$ and $A$ to $C$ lie completely within the plane.

* **First in-plane vector ($\overrightarrow{AB}$):**

$$
\overrightarrow{AB} = B - A = (2 - 1, \ 1 - 0, \ 0 - 2) = (1, 1, -2)
$$

* **Second in-plane vector ($\overrightarrow{AC}$):**

$$
\overrightarrow{AC} = C - A = (0 - 1, \ 3 - 0, \ 1 - 2) = (-1, 3, -1)
$$

*(Note: Because $\overrightarrow{AB}$ and $\overrightarrow{AC}$ are not scalar multiples of each other, they are linearly independent and uniquely span the entire plane.)*

### 2. Finding a Normal Vector Perpendicular to Both ($\mathbf{n} = \overrightarrow{AB} \times \overrightarrow{AC}$)

**Mechanism Used:** 3D vector cross product via cofactor expansion of the symbolic $3 \times 3$ determinant formed by $(\mathbf{i}, \mathbf{j}, \mathbf{k})$, $\overrightarrow{AB} = (1, 1, -2)$, and $\overrightarrow{AC} = (-1, 3, -1)$:

$$
\begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
1 & 1 & -2 \\
-1 & 3 & -1
\end{vmatrix}
$$

Evaluate each $2 \times 2$ minor determinant:

* **$\mathbf{i}$-component:**

$$
\begin{vmatrix}
1 & -2 \\
3 & -1
\end{vmatrix}
= (1)(-1) - (-2)(3) = -1 - (-6) = 5
$$

* **$\mathbf{j}$-component (with alternating minus sign):**

$$
-\begin{vmatrix}
1 & -2 \\
-1 & -1
\end{vmatrix}
= -\big((1)(-1) - (-2)(-1)\big) = -(-1 - 2) = -(-3) = 3
$$

* **$\mathbf{k}$-component:**

$$
\begin{vmatrix}
1 & 1 \\
-1 & 3
\end{vmatrix}
= (1)(3) - (1)(-1) = 3 - (-1) = 4
$$

Combining the three components gives a normal vector to the plane:

$$
\mathbf{n} = \overrightarrow{AB} \times \overrightarrow{AC} = (5, 3, 4)
$$

### 3. Checking Perpendicularity Using Dot Products

**Mechanism Used:** Orthogonality criterion ($u \cdot v = 0 \iff u \perp v$). We verify that $\mathbf{n} \cdot \overrightarrow{AB} = 0$ and $\mathbf{n} \cdot \overrightarrow{AC} = 0$.

* **Check 1 — Dot product with $\overrightarrow{AB} = (1, 1, -2)$:**

$$
\mathbf{n} \cdot \overrightarrow{AB} = (5)(1) + (3)(1) + (4)(-2) = 5 + 3 - 8 = 0
$$

* **Check 2 — Dot product with $\overrightarrow{AC} = (-1, 3, -1)$:**

$$
\mathbf{n} \cdot \overrightarrow{AC} = (5)(-1) + (3)(3) + (4)(-1) = -5 + 9 - 4 = 0
$$

* **Bonus Check — Third edge $\overrightarrow{BC} = C - B = (-2, 2, 1)$:**

$$
\mathbf{n} \cdot \overrightarrow{BC} = (5)(-2) + (3)(2) + (4)(1) = -10 + 6 + 4 = 0
$$

### 4. Geometric Interpretation

In $\mathbb{R}^3$, two non-collinear vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$ define a flat 2D surface (a plane). Taking their cross product produces a **normal vector** $\mathbf{n} = (5, 3, 4)$ that rises straight out of that surface at a $90^\circ$ right angle to *every* line segment inside the plane (including $\overrightarrow{AB}$, $\overrightarrow{AC}$, and $\overrightarrow{BC}$). This normal vector uniquely fixes the tilt/orientation of the plane in 3D space (giving the plane equation $5(x - 1) + 3(y - 0) + 4(z - 2) = 0$, or $5x + 3y + 4z = 13$).

<img width="1408" height="768" alt="image" src="https://github.com/user-attachments/assets/5f4b1407-30ef-4efc-a424-c1808380af1b" />
