## Question

Exercise 10. Triangle Area from Vectors
The points $A = (0, 0, 0)$, $B = (2, 1, 0)$, and $C = (1, 3, 2)$ form a triangle. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$, compute the area of the parallelogram using the cross product, and then find the area of the triangle. Explain the factor $\frac{1}{2}$.

## Solution

### 1. Constructing the Side Vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$

**Mechanism Used:** Displacement vector construction (head-minus-tail rule, $\overrightarrow{PQ} = Q - P$) anchored at the shared vertex $A = (0, 0, 0)$ so both side vectors originate from the same corner of the triangle.

* **Vector $\overrightarrow{AB}$:**

$$\overrightarrow{AB} = B - A = (2 - 0, \ 1 - 0, \ 0 - 0) = (2, 1, 0)$$

* **Vector $\overrightarrow{AC}$:**

$$\overrightarrow{AC} = C - A = (1 - 0, \ 3 - 0, \ 2 - 0) = (1, 3, 2)$$

### 2. Computing the Cross Product $\overrightarrow{AB} \times \overrightarrow{AC}$

**Mechanism Used:** 3D cross product via cofactor expansion of the symbolic $3 \times 3$ determinant formed by $(\mathbf{i}, \mathbf{j}, \mathbf{k})$, $\overrightarrow{AB} = (2, 1, 0)$, and $\overrightarrow{AC} = (1, 3, 2)$:

$$\begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 2 & 1 & 0 \\ 1 & 3 & 2 \end{vmatrix}$$

Evaluate each $2 \times 2$ minor determinant:

* **$\mathbf{i}$-component:**

$$\begin{vmatrix} 1 & 0 \\ 3 & 2 \end{vmatrix} = (1)(2) - (0)(3) = 2 - 0 = 2$$

* **$\mathbf{j}$-component (with alternating minus sign):**

$$-\begin{vmatrix} 2 & 0 \\ 1 & 2 \end{vmatrix} = -\big((2)(2) - (0)(1)\big) = -(4 - 0) = -4$$

* **$\mathbf{k}$-component:**

$$\begin{vmatrix} 2 & 1 \\ 1 & 3 \end{vmatrix} = (2)(3) - (1)(1) = 6 - 1 = 5$$

Combining the three components gives the normal vector:

$$\overrightarrow{AB} \times \overrightarrow{AC} = (2, -4, 5)$$

**Orthogonality Check:** Verify that $(2, -4, 5)$ is perpendicular to both $\overrightarrow{AB}$ and $\overrightarrow{AC}$:

$$(2, -4, 5) \cdot (2, 1, 0) = 4 - 4 + 0 = 0, \quad (2, -4, 5) \cdot (1, 3, 2) = 2 - 12 + 10 = 0$$

### 3. Computing the Area of the Parallelogram

**Mechanism Used:** Geometric magnitude property of the cross product—the Euclidean norm $\Vert{}\overrightarrow{AB} \times \overrightarrow{AC}\Vert{}$ equals the exact area of the parallelogram spanned by $\overrightarrow{AB}$ and $\overrightarrow{AC}$:

$$\mathrm{Area}_{\mathrm{parallelogram}} = \Vert{}\overrightarrow{AB} \times \overrightarrow{AC}\Vert{} = \sqrt{2^2 + (-4)^2 + 5^2}$$

$$\mathrm{Area}_{\mathrm{parallelogram}} = \sqrt{4 + 16 + 25} = \sqrt{45} = 3\sqrt{5} \approx 6.708$$

### 4. Finding the Area of Triangle $\triangle ABC$

**Mechanism Used:** Half-parallelogram area formula for a triangle spanned by two adjacent vectors:

$$\mathrm{Area}_{\triangle ABC} = \frac{1}{2} \Vert{}\overrightarrow{AB} \times \overrightarrow{AC}\Vert{}$$

Substituting $\Vert{}\overrightarrow{AB} \times \overrightarrow{AC}\Vert{} = \sqrt{45} = 3\sqrt{5}$:

$$\mathrm{Area}_{\triangle ABC} = \frac{\sqrt{45}}{2} = \frac{3\sqrt{5}}{2} \approx 3.354$$

**Verification Check (Using Law of Cosines / Dot Product):**

We can double-check this area using $\mathrm{Area}_{\triangle ABC} = \frac{1}{2}\Vert{}\overrightarrow{AB}\Vert{}\Vert{}\overrightarrow{AC}\Vert{}\sin\theta$:

* $\Vert{}\overrightarrow{AB}\Vert{} = \sqrt{2^2 + 1^2 + 0^2} = \sqrt{5}$ and $\Vert{}\overrightarrow{AC}\Vert{} = \sqrt{1^2 + 3^2 + 2^2} = \sqrt{14}$.
*
