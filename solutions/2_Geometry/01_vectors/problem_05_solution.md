## Question

Exercise 5. Angle Between Vectors
Given $u = (1, 1, 0)$ and $v = (1, 0, 1)$:

1. Use the sign of $u \cdot v$ to predict the type of angle.
2. Compute the angle.
3. Compare the result with the prediction.

## Solution

### 1. Predicting the Type of Angle Using the Sign of $u \cdot v$

**Mechanism Used:** Component-wise dot product ($u \cdot v = u_1 v_1 + u_2 v_2 + u_3 v_3$) combined with the geometric sign rule ($u \cdot v = \|u\|\|v\|\cos\theta$). Because vector magnitudes $\|u\|$ and $\|v\|$ are strictly positive for non-zero vectors, the sign of $u \cdot v$ matches the sign of $\cos\theta$:

* $u \cdot v > 0 \implies \cos\theta > 0 \implies$ **Acute angle** ($0^\circ \le \theta < 90^\circ$)
* $u \cdot v = 0 \implies \cos\theta = 0 \implies$ **Right angle** ($\theta = 90^\circ$)
* $u \cdot v < 0 \implies \cos\theta < 0 \implies$ **Obtuse angle** ($90^\circ < \theta \le 180^\circ$)

Compute $u \cdot v$ for $u = (1, 1, 0)$ and $v = (1, 0, 1)$:

$$
u \cdot v = (1)(1) + (1)(0) + (0)(1) = 1 + 0 + 0 = 1
$$

**Prediction:** Since $u \cdot v = 1 > 0$, we predict that the angle $\theta$ between $u$ and $v$ is **acute** ($0^\circ < \theta < 90^\circ$).

### 2. Computing the Exact Angle $\theta$

**Mechanism Used:** Inverse cosine formula derived from the geometric dot product:

$$
\cos\theta = \frac{u \cdot v}{\|u\|\|v\|}
$$

**Step 1: Compute the Euclidean norms $\|u\|$ and $\|v\|$.**

$$
\|u\| = \sqrt{1^2 + 1^2 + 0^2} = \sqrt{2}
$$

$$
\|v\| = \sqrt{1^2 + 0^2 + 1^2} = \sqrt{2}
$$

**Step 2: Substitute $u \cdot v = 1$, $\|u\| = \sqrt{2}$, and $\|v\| = \sqrt{2}$ into the cosine formula.**

$$
\cos\theta = \frac{1}{\sqrt{2} \cdot \sqrt{2}} = \frac{1}{2}
$$

**Step 3: Apply $\arccos$ to find $\theta$.**

$$
\theta = \arccos\left(\frac{1}{2}\right) = \frac{\pi}{3} \text{ radians} = 60^\circ
$$

### 3. Comparing the Result with the Prediction & Geometric Check

* **Comparison:** The computed angle $\theta = 60^\circ$ ($\frac{\pi}{3}$ rad) satisfies $0^\circ < 60^\circ < 90^\circ$, so it is indeed an **acute angle**, matching our initial sign-based prediction.
* **Geometric Check:** The vectors $u = (1, 1, 0)$ and $v = (1, 0, 1)$ are two face diagonals of a unit cube sharing the origin $(0, 0, 0)$. The third edge connecting their tips has vector $u - v = (0, 1, -1)$ with length $\|u - v\| = \sqrt{0^2 + 1^2 + (-1)^2} = \sqrt{2}$. Because all three sides have equal length $\sqrt{2}$, the origin and the two tips form an **equilateral triangle**, whose interior angles are all guaranteed to be $60^\circ$.
