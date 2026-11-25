## Question

Exercise 2. Distance as the Length of a Vector
The points are $A = (1, 2, 3)$ and $B = (4, -2, 6)$.

1. Construct $\overrightarrow{AB}$.
2. Compute its length.
3. Compute the distance between the points using the coordinate formula.
4. Explain why both calculations give the same result.

## Solution

### 1. Constructing the Displacement Vector $\overrightarrow{AB}$

**Mechanism Used:** Displacement vector construction (head-minus-tail rule). To find the vector directed from initial point $A = (x_1, y_1, z_1)$ to terminal point $B = (x_2, y_2, z_2)$, we subtract the coordinates of $A$ from the coordinates of $B$:

$$
\overrightarrow{AB} = B - A = (x_2 - x_1, \ y_2 - y_1, \ z_2 - z_1)
$$

Substituting $A = (1, 2, 3)$ and $B = (4, -2, 6)$:

$$
\overrightarrow{AB} = (4 - 1, \ -2 - 2, \ 6 - 3) = (3, -4, 3)
$$

### 2. Computing the Length (Norm) of $\overrightarrow{AB}$

**Mechanism Used:** Euclidean norm ($L_2$-norm) of a vector $\mathbf{v} = (v_1, v_2, v_3)$, defined as $\|\mathbf{v}\| = \sqrt{v_1^2 + v_2^2 + v_3^2}$.

Applying this definition to $\overrightarrow{AB} = (3, -4, 3)$:

$$
\|\overrightarrow{AB}\| = \sqrt{3^2 + (-4)^2 + 3^2}
$$

$$
\|\overrightarrow{AB}\| = \sqrt{9 + 16 + 9} = \sqrt{34} \approx 5.831
$$

### 3. Computing the Distance Using the Coordinate Formula

**Mechanism Used:** 3D Euclidean distance formula between two points $A = (x_1, y_1, z_1)$ and $B = (x_2, y_2, z_2)$:

$$
d(A, B) = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2 + (z_2 - z_1)^2}
$$

Substituting the coordinates of $A = (1, 2, 3)$ and $B = (4, -2, 6)$ directly:

$$
d(A, B) = \sqrt{(4 - 1)^2 + (-2 - 2)^2 + (6 - 3)^2}
$$

$$
d(A, B) = \sqrt{3^2 + (-4)^2 + 3^2} = \sqrt{9 + 16 + 9} = \sqrt{34} \approx 5.831
$$

**Verification Check:** Notice that the squared terms inside the radical ($9$, $16$, and $9$) and the final value ($\sqrt{34}$) match the vector norm calculation in Step 2 identically. Additionally, reversing the direction to $\overrightarrow{BA} = (-3, 4, -3)$ yields $\|\overrightarrow{BA}\| = \sqrt{(-3)^2 + 4^2 + (-3)^2} = \sqrt{34}$, confirming symmetry of distance.

### 4. Why Both Calculations Give the Same Result (Geometric & Algebraic Interpretation)

* **Algebraic Identity:** By definition, the components of $\overrightarrow{AB}$ are $(v_1, v_2, v_3) = (x_2 - x_1, \ y_2 - y_1, \ z_2 - z_1)$. Therefore, taking the norm $\|\overrightarrow{AB}\| = \sqrt{v_1^2 + v_2^2 + v_3^2}$ is algebraically the exact same computation as substituting coordinate differences into the distance formula.
* **Geometric Interpretation:** Translating the directed line segment from $A$ to $B$ so that its tail rests at the origin $(0, 0, 0)$ preserves its length and orientation. In 3D space, both formulas apply the **Pythagorean theorem twice** across the orthogonal coordinate axes ($\Delta x$, $\Delta y$, and $\Delta z$) to measure the straight-line length of the diagonal of a rectangular box with side lengths $3$, $4$, and $3$.
