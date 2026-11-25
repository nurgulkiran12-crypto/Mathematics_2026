## Question

Exercise 14. Closest Point on a Line
Given a point $P = (4, 1)$ and a line through the origin with direction $v = (1, 2)$. Using projection, find the closest point on the line, the distance from $P$ to the line, and verify that the appropriate vector is perpendicular to the direction of the line.

## Solution

### 1. Finding the Closest Point on the Line via Orthogonal Projection

**Mechanism Used:** Orthogonal projection of the position vector $p = \overrightarrow{OP} = (4, 1)$ onto the line's direction vector $v = (1, 2)$ anchored at the origin $O = (0, 0)$:

$$
\mathrm{proj}_v p = \frac{p \cdot v}{v \cdot v} v
$$

**Step 1: Compute the dot products $p \cdot v$ and $v \cdot v$.**

$$
p \cdot v = (4)(1) + (1)(2) = 4 + 2 = 6
$$

$$
v \cdot v = \|v\|^2 = 1^2 + 2^2 = 1 + 4 = 5
$$

**Step 2: Multiply the scalar projection factor by $v$.**

$$
\mathrm{proj}_v p = \frac{6}{5}(1, 2) = \left(\frac{6}{5}, \frac{12}{5}\right) = (1.2, 2.4)
$$

Because the line passes through the origin, the tip of the projected vector gives the exact coordinates of the **closest point** $Q$ on the line:

$$
Q = \left(\frac{6}{5}, \frac{12}{5}\right) = (1.2, 2.4)
$$

### 2. Computing the Distance from $P$ to the Line

**Mechanism Used:** Euclidean norm of the orthogonal residual vector $r = \overrightarrow{QP} = p - \mathrm{proj}_v p$, which measures the shortest perpendicular distance from $P$ to the line.

**Step 1: Construct the residual vector $r = p - \mathrm{proj}_v p$.**

$$
r = (4, 1) - \left(\frac{6}{5}, \frac{12}{5}\right) = \left(\frac{20}{5} - \frac{6}{5}, \ \frac{5}{5} - \frac{12}{5}\right) = \left(\frac{14}{5}, -\frac{7}{5}\right) = (2.8, -1.4)
$$

**Step 2: Compute the Euclidean norm $\|r\|$.**

$$
d(P, \text{line}) = \|r\| = \sqrt{\left(\frac{14}{5}\right)^2 + \left(-\frac{7}{5}\right)^2} = \sqrt{\frac{196}{25} + \frac{49}{25}} = \sqrt{\frac{245}{25}}
$$

Simplify the radical ($\sqrt{245} = \sqrt{49 \cdot 5} = 7\sqrt{5}$):

$$
d(P, \text{line}) = \frac{7\sqrt{5}}{5} \approx 3.130
$$

**Independent Verification Check (2D Point-to-Line Distance Formula):**

The line through $(0, 0)$ with direction $v = (1, 2)$ has slope $m = 2$, giving the Cartesian equation $2x - y = 0$. Applying the standard point-to-line distance formula $d = \frac{|Ax_0 + By_0 + C|}{\sqrt{A^2 + B^2}}$ at $P = (4, 1)$:

$$
d = \frac{|2(4) - 1(1) + 0|}{\sqrt{2^2 + (-1)^2}} = \frac{|8 - 1|}{\sqrt{5}} = \frac{7}{\sqrt{5}} = \frac{7\sqrt{5}}{5}
$$

Both methods produce the exact same distance, confirming our projection calculation.

### 3. Verifying Perpendicularity ($r \cdot v = 0$) & Geometric Interpretation

**Mechanism Used:** Orthogonality criterion via the dot product ($r \cdot v = 0 \iff r \perp v$).

Check the dot product between the residual vector $r = \overrightarrow{QP} = \left(\frac{14}{5}, -\frac{7}{5}\right)$ and the line's direction vector $v = (1, 2)$:

$$
r \cdot v = \left(\frac{14}{5}\right)(1) + \left(-\frac{7}{5}\right)(2) = \frac{14}{5} - \frac{14}{5} = 0
$$

**Geometric Interpretation:**

* **Why Perpendicularity Guarantees the Closest Point:** For any other point $X$ on the line ($X \neq Q$), the points $Q$, $X$, and $P$ form a **right triangle** $\triangle PQX$ with a $90^\circ$ angle at $Q$ (since $\overrightarrow{QP} \perp \overrightarrow{QX}$). By the Pythagorean theorem, $\| \overrightarrow{XP} \|^2 = \| \overrightarrow{QP} \|^2 + \| \overrightarrow{QX} \|^2 > \| \overrightarrow{QP} \|^2$, proving geometrically that the foot of the perpendicular $Q = (1.2, 2.4)$ is strictly the closest point on the line to $P$.
