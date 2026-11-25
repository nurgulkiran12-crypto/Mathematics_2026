## Question

Exercise 6. Projection and Perpendicular Component
Find the projection of $u = (4, 2)$ onto the direction $v = (1, 1)$. Then compute:

$$
r = u - \operatorname{proj}_v u
$$

and verify that $r \cdot v = 0$. Explain this result geometrically.

## Solution

### 1. Computing the Orthogonal Projection $\operatorname{proj}_v u$

**Mechanism Used:** Orthogonal projection formula of a vector $u$ onto a non-zero direction vector $v$:

$$
\operatorname{proj}_v u = \frac{u \cdot v}{v \cdot v} v
$$

**Step 1: Compute the dot products $u \cdot v$ and $v \cdot v$.**

For $u = (4, 2)$ and $v = (1, 1)$:

$$
u \cdot v = (4)(1) + (2)(1) = 4 + 2 = 6
$$

$$
v \cdot v = \|v\|^2 = 1^2 + 1^2 = 1 + 1 = 2
$$

**Step 2: Multiply the scalar projection ratio by $v$.**

$$
\operatorname{proj}_v u = \frac{6}{2}(1, 1) = 3(1, 1) = (3, 3)
$$

### 2. Computing the Perpendicular (Residual) Component $r$

**Mechanism Used:** Orthogonal vector decomposition ($u = \operatorname{proj}_v u + r$), isolating the component of $u$ orthogonal to $v$ by subtracting the parallel projection from the original vector:

$$
r = u - \operatorname{proj}_v u
$$

Substituting $u = (4, 2)$ and $\operatorname{proj}_v u = (3, 3)$:

$$
r = (4, 2) - (3, 3) = (4 - 3, \ 2 - 3) = (1, -1)
$$

### 3. Verifying Orthogonality ($r \cdot v = 0$) and Decomposition

Compute the dot product of $r = (1, -1)$ and $v = (1, 1)$:

$$
r \cdot v = (1)(1) + (-1)(1) = 1 - 1 = 0
$$

**Additional Reconstruction Check:** Adding the parallel and perpendicular parts reconstructs $u$ identically:

$$
\operatorname{proj}_v u + r = (3, 3) + (1, -1) = (4, 2) = u
$$

Because $r \cdot v = 0$, the residual vector $r$ is strictly perpendicular to $v$.

### 4. Geometric Explanation

Geometrically, orthogonal projection decomposes any vector $u$ into two mutually perpendicular components relative to the line spanned by $v$:

* **Shadow Along $v$ ($\operatorname{proj}_v u = (3, 3)$):** Dropping a perpendicular line from the tip of $u = (4, 2)$ onto the line along $v = (1, 1)$ (the line $y = x$) lands at the closest point $(3, 3)$ on that line. This is the component of $u$ acting purely in the direction of $v$.
* **Perpendicular Drop ($r = (1, -1)$):** The residual vector $r$ connects the shadow $(3, 3)$ straight up to the tip of $u = (4, 2)$. Because it represents the **shortest distance** from the tip of $u$ to the line spanned by $v$, it meets that line at a $90^\circ$ right angle ($r \cdot v = 0$), forming a right triangle with hypotenuse $u$ and legs $\operatorname{proj}_v u$ and $r$.
