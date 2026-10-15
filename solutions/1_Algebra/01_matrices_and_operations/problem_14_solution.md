# Exercise 14: Rotation Matrices

Let's explore rotation matrices and verify how matrix multiplication corresponds to adding angles geometrically!

---

Given the rotation matrix for angle $\theta$:

$$
R(\theta) = \begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix}
$$

---

## Step 1: Computing $R(\alpha)R(\beta)$

Let's multiply $R(\alpha)$ by $R(\beta)$:

$$
R(\alpha)R(\beta) = \begin{pmatrix} \cos\alpha & -\sin\alpha \\ \sin\alpha & \cos\alpha \end{pmatrix} \begin{pmatrix} \cos\beta & -\sin\beta \\ \sin\beta & \cos\beta \end{pmatrix}
$$

Calculating each entry using standard matrix multiplication:

**Top-left entry:**

$$
\cos\alpha\cos\beta - \sin\alpha\sin\beta
$$

**Top-right entry:**

$$
-\cos\alpha\sin\beta - \sin\alpha\cos\beta = -(\sin\alpha\cos\beta + \cos\alpha\sin\beta)
$$

**Bottom-left entry:**

$$
\sin\alpha\cos\beta + \cos\alpha\sin\beta
$$
**Bottom-right entry:**

$$
-\sin\alpha\sin\beta + \cos\alpha\cos\beta = \cos\alpha\cos\beta - \sin\alpha\sin\beta
$$

Putting these entries into the resulting matrix:

$$
R(\alpha)R(\beta) = \begin{pmatrix} \cos\alpha\cos\beta - \sin\alpha\sin\beta & -(\sin\alpha\cos\beta + \cos\alpha\sin\beta) \\ \sin\alpha\cos\beta + \cos\alpha\sin\beta & \cos\alpha\cos\beta - \sin\alpha\sin\beta \end{pmatrix}
$$

---

## Step 2: Applying Angle-Sum Identities

Using the standard trigonometric angle-sum formulas:

* $\cos(\alpha + \beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta$
* $\sin(\alpha + \beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta$

Substitute these identities into our resulting matrix:

$$
R(\alpha)R(\beta) = \begin{pmatrix} \cos(\alpha+\beta) & -\sin(\alpha+\beta) \\ \sin(\alpha+\beta) & \cos(\alpha+\beta) \end{pmatrix}
$$

This is precisely the definition of $R(\alpha + \beta)$! Thus, we have verified that:

$$
R(\alpha)R(\beta) = R(\alpha+\beta)
$$

---

## Step 3: Geometric Explanation

Geometrically, multiplying rotation matrices represents **composing successive rotations**. Rotating a vector first by angle $\beta$ and then rotating that new result by angle $\alpha$ is completely equivalent to performing a single rotation by the combined angle $(\alpha + \beta)$.
