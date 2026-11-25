## Question

Exercise 3. Vector Normalization
For $v = (3, 4)$ find a unit vector $e$ with the same direction and orientation. Check that $\|e\| = 1$, reconstruct $v$ in the form $v = \|v\|e$, and explain what changes during normalization and what remains unchanged.

## Solution

### 1. Computing the Magnitude (Norm) of $v$

**Mechanism Used:** 2D Euclidean norm ($L_2$-norm) formula $\|v\| = \sqrt{v_1^2 + v_2^2}$ to measure the length of the vector before scaling.

For $v = (3, 4)$:

$$
\|v\| = \sqrt{3^2 + 4^2} = \sqrt{9 + 16} = \sqrt{25} = 5
$$

### 2. Finding the Unit Vector $e$ (Normalization)

**Mechanism Used:** Scalar multiplication by the positive reciprocal of the vector's magnitude ($e = \frac{1}{\|v\|} v$). Dividing each component by $\|v\|$ rescales the vector to unit length without reversing its orientation.

Substituting $v = (3, 4)$ and $\|v\| = 5$:

$$
e = \frac{1}{5}(3, 4) = \left(\frac{3}{5}, \frac{4}{5}\right) = (0.6, 0.8)
$$

### 3. Verification Check ($\|e\| = 1$)

Compute the Euclidean norm of $e = \left(\frac{3}{5}, \frac{4}{5}\right)$ to verify that its length equals $1$:

$$
\|e\| = \sqrt{\left(\frac{3}{5}\right)^2 + \left(\frac{4}{5}\right)^2} = \sqrt{\frac{9}{25} + \frac{16}{25}} = \sqrt{\frac{25}{25}} = \sqrt{1} = 1
$$

The norm equals $1$, confirming that $e$ is a valid unit vector.

### 4. Reconstructing $v$ in Polar/Magnitude-Direction Form ($v = \|v\|e$)

**Mechanism Used:** Scalar multiplication of the unit direction vector $e$ by the original scalar magnitude $\|v\|$:

$$
\|v\|e = 5 \cdot \left(\frac{3}{5}, \frac{4}{5}\right) = \left(5 \cdot \frac{3}{5}, \ 5 \cdot \frac{4}{5}\right) = (3, 4) = v
$$

This confirms that any non-zero vector decomposes cleanly into the product of its magnitude ($\|v\| = 5$) and its pure direction ($e = (0.6, 0.8)$).

### 5. Geometric Interpretation: What Changes vs. What Remains Unchanged

* **What Changes:** Only the **length (magnitude)** of the vector changes—it is compressed from $\|v\| = 5$ down to $\|e\| = 1$, placing the tip of $e$ directly on the **unit circle** ($x^2 + y^2 = 1$).
* **What Remains Unchanged:** The **direction (line of action)** and **orientation (sense/pointing direction)** remain completely unchanged. Because we multiplied by a strictly positive scalar ($\frac{1}{5} > 0$), the vector still lies along the exact same ray from the origin at the exact same angle ($\theta = \arctan\left(\frac{4}{3}\right) \approx 53.13^\circ$) in the first quadrant.
