<img width="1408" height="768" alt="image" src="https://github.com/user-attachments/assets/d1bd13d6-01d0-457e-a834-cd08377b3e44" />
## Question

Exercise 11. Decomposition into Parallel and Perpendicular Components
Decompose $u = (3, 4)$ into components parallel and perpendicular to $v = (1, 2)$. Check:

$$
u = u_{\parallel} + u_{\perp}, \quad u_{\perp} \cdot v = 0
$$

Explain why these are two independent checks of correctness.

## Solution

### 1. Computing the Parallel Component $u_{\parallel}$

**Mechanism Used:** Orthogonal vector projection formula onto a non-zero direction vector $v$:

$$
u_{\parallel} = \frac{u \cdot v}{v \cdot v} v
$$

Compute the required dot products for $u = (3, 4)$ and $v = (1, 2)$:

$$
u \cdot v = (3)(1) + (4)(2) = 3 + 8 = 11
$$

$$
v \cdot v = \|v\|^2 = 1^2 + 2^2 = 1 + 4 = 5
$$

Substitute these values into the projection formula:

$$
u_{\parallel} = \frac{11}{5}(1, 2) = \left(\frac{11}{5}, \frac{22}{5}\right) = (2.2, 4.4)
$$

### 2. Computing the Perpendicular Component $u_{\perp}$

**Mechanism Used:** Orthogonal residual subtraction ($u_{\perp} = u - u_{\parallel}$), isolating the component of $u$ orthogonal to $v$:

$$
u_{\perp} = (3, 4) - \left(\frac{11}{5}, \frac{22}{5}\right) = \left(\frac{15}{5} - \frac{11}{5}, \ \frac{20}{5} - \frac{22}{5}\right) = \left(\frac{4}{5}, -\frac{2}{5}\right) = (0.8, -0.4)
$$

### 3. Performing the Two Verification Checks

**Check 1 — Reconstruction ($u = u_{\parallel} + u_{\perp}$):**

$$
u_{\parallel} + u_{\perp} = \left(\frac{11}{5}, \frac{22}{5}\right) + \left(\frac{4}{5}, -\frac{2}{5}\right) = \left(\frac{15}{5}, \frac{20}{5}\right) = (3, 4) = u
$$

**Check 2 — Orthogonality ($u_{\perp} \cdot v = 0$):**

$$
u_{\perp} \cdot v = \left(\frac{4}{5}\right)(1) + \left(-\frac{2}{5}\right)(2) = \frac{4}{5} - \frac{4}{5} = 0
$$

Both conditions hold exactly. Geometrically, $u_{\parallel} = (2.2, 4.4)$ lies along the line of $v = (1, 2)$, and $u_{\perp} = (0.8, -0.4)$ meets that line at a $90^\circ$ right angle so the two parts form the legs of a right triangle with hypotenuse $u$.

### 4. Why These Are Two Independent Checks of Correctness

* **First Check ($u = u_{\parallel} + u_{\perp}$) Tests Vector Closure / Sum Completeness:** Adding any vector $w$ to $u - w$ automatically equals $u$ for *any* arbitrary vector $w$. Therefore, $u_{\parallel} + u_{\perp} = u$ only confirms that our subtraction $u - u_{\parallel}$ did not introduce an arithmetic error—it does **not** prove that $u_{\parallel}$ lies in the direction of $v$ or that $u_{\perp}$ is perpendicular to $v$.
* **Second Check ($u_{\perp} \cdot v = 0$) Tests Geometric Orthogonality:** Taking the dot product of $u_{\perp}$ with $v$ checks that the angle between the residual and the reference direction is $90^\circ$. An arithmetic mistake in $u_{\parallel}$ (such as using the wrong scalar ratio) would leave a non-zero projection error inside $u_{\perp}$, causing $u_{\perp} \cdot v \neq 0$ even when $u_{\parallel} + u_{\perp} = u$ still holds.

Together, the two checks verify both **algebraic consistency** (the pieces sum back to $u$) and **geometric orthogonality** (the split is genuinely perpendicular to $v$).
