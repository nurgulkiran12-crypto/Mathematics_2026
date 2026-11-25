## Question

Exercise 13. Do Four Points Lie in One Plane?
Given $A = (0, 0, 0)$, $B = (1, 2, 0)$, $C = (0, 1, 1)$, $D = (2, 5, 1)$.

1. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$.
2. Find $\mathbf{n} = \overrightarrow{AB} \times \overrightarrow{AC}$.
3. Construct $\overrightarrow{AD}$ and check whether $\overrightarrow{AD} \cdot \mathbf{n} = 0$.
4. Based on this, decide whether $D$ lies in the plane determined by $A, B, C$, and justify the criterion.

## Solution

### 1. Constructing $\overrightarrow{AB}$ and $\overrightarrow{AC}$

**Mechanism Used:** Displacement vector construction (head-minus-tail rule, $\overrightarrow{PQ} = Q - P$) anchored at the common origin vertex $A = (0, 0, 0)$ so both vectors lie inside the plane determined by $A$, $B$, and $C$.

* **Vector $\overrightarrow{AB}$:**

$$
\overrightarrow{AB} = B - A = (1 - 0, \ 2 - 0, \ 0 - 0) = (1, 2, 0)
$$

* **Vector $\overrightarrow{AC}$:**

$$
\overrightarrow{AC} = C - A = (0 - 0, \ 1 - 0, \ 1 - 0) = (0, 1, 1)
$$

*(Since $\overrightarrow{AB}$ and $\overrightarrow{AC}$ are not scalar multiples of each other, they are linearly independent and uniquely define a plane.)*

### 2. Finding the Normal Vector $\mathbf{n} = \overrightarrow{AB} \times \overrightarrow{AC}$

**Mechanism Used:** 3D cross product via cofactor expansion of the symbolic $3 \times 3$ determinant formed by $(\mathbf{i}, \mathbf{j}, \mathbf{k})$, $\overrightarrow{AB} = (1, 2, 0)$, and $\overrightarrow{AC} = (0, 1, 1)$:

$$
\begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
1 & 2 & 0 \\
0 & 1 & 1
\end{vmatrix}
$$

Evaluate each $2 \times 2$ minor determinant:

* **$\mathbf{i}$-component:**

$$
\begin{vmatrix}
2 & 0 \\
1 & 1
\end{vmatrix}
= (2)(1) - (0)(1) = 2 - 0 = 2
$$

* **$\mathbf{j}$-component (with alternating minus sign):**

$$
-\begin{vmatrix}
1 & 0 \\
0 & 1
\end{vmatrix}
= -\big((1)(1) - (0)(0)\big) = -(1 - 0) = -1
$$

* **$\mathbf{k}$-component:**

$$
\begin{vmatrix}
1 & 2 \\
0 & 1
\end{vmatrix}
= (1)(1) - (2)(0) = 1 - 0 = 1
$$

Combining all three components yields the plane's normal vector:

$$
\mathbf{n} = \overrightarrow{AB} \times \overrightarrow{AC} = (2, -1, 1)
$$

**Orthogonality Check:** Verify that $\mathbf{n} = (2, -1, 1)$ is perpendicular to both $\overrightarrow{AB}$ and $\overrightarrow{AC}$:

$$
\mathbf{n} \cdot \overrightarrow{AB} = (2)(1) + (-1)(2) + (1)(0) = 2 - 2 + 0 = 0
$$

$$
\mathbf{n} \cdot \overrightarrow{AC} = (2)(0) + (-1)(1) + (1)(1) = 0 - 1 + 1 = 0
$$

### 3. Constructing $\overrightarrow{AD}$ and Checking $\overrightarrow{AD} \cdot \mathbf{n} = 0$

**Mechanism Used:** Displacement vector construction for $\overrightarrow{AD}$ followed by the scalar triple product $\overrightarrow{AD} \cdot (\overrightarrow{AB} \times \overrightarrow{AC})$.

* **Constructing $\overrightarrow{AD}$:**

$$
\overrightarrow{AD} = D - A = (2 - 0, \ 5 - 0, \ 1 - 0) = (2, 5, 1)
$$

* **Computing $\overrightarrow{AD} \cdot \mathbf{n}$:**

$$
\overrightarrow{AD} \cdot \mathbf{n} = (2)(2) + (5)(-1) + (1)(1) = 4 - 5 + 1 = 0
$$

Yes, the dot product equals **$0$**.

### 4. Decision and Justification of the Coplanarity Criterion

**Decision:** **Yes**, the point $D = (2, 5, 1)$ **lies in the plane** determined by $A$, $B$, and $C$ (all four points are coplanar).

**Justification (Algebraic & Geometric Interpretation):**

* **Orthogonality to the Plane's Normal:** The plane through $A$, $B$, and $C$ consists precisely of all points $P$ such that the displacement vector $\overrightarrow{AP}$ is perpendicular to the plane's normal vector $\mathbf{n} = \overrightarrow{AB} \times \overrightarrow{AC}$ (giving the plane equation $2x - y + z = 0$). Because $\overrightarrow{AD} \cdot \mathbf{n} = 0$, the vector $\overrightarrow{AD}$ has zero component in the normal direction and lies completely flat inside the plane.
* **Zero Parallelepiped Volume (Scalar Triple Product):** Geometrically, the absolute value $|\overrightarrow{AD} \cdot (\overrightarrow{AB} \times \overrightarrow{AC})|$ equals the **volume of the 3D parallelepiped** spanned by $\overrightarrow{AB}$, $\overrightarrow{AC}$, and $\overrightarrow{AD}$. Because this volume is $0$, the parallelepiped is completely flattened—meaning $\overrightarrow{AD}$ can be written as a linear combination of $\overrightarrow{AB}$ and $\overrightarrow{AC}$ (specifically, $\overrightarrow{AD} = 2\overrightarrow{AB} + 1\overrightarrow{AC} = 2(1, 2, 0) + 1(0, 1, 1) = (2, 5, 1)$), which serves as an independent algebraic check confirming $D$ is in the plane.

<img width="1408" height="768" alt="image" src="https://github.com/user-attachments/assets/2d7319f7-0271-4174-82b5-3cecd0a4c595" />
