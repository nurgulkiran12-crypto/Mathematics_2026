# Exercise 9: Composing Transformations

Given:

$$
S = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix}, \qquad R = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}, \qquad x = \begin{pmatrix} 1 \\ 2 \end{pmatrix}
$$

---

## Step 1: Computing $RSx$ (Scaling First, Then Rotation)

First, apply the scaling matrix $S$ to vector $x$:

$$
Sx = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} 2(1) + 0(2) \\ 0(1) + 1(2) \end{pmatrix} = \begin{pmatrix} 2 \\ 2 \end{pmatrix}
$$

Next, apply the rotation matrix $R$ to the resulting vector:

$$
RSx = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 2 \\ 2 \end{pmatrix} = \begin{pmatrix} 0(2) + (-1)(2) \\ 1(2) + 0(2) \end{pmatrix} = \begin{pmatrix} -2 \\ 2 \end{pmatrix}
$$

---

## Step 2: Computing $SRx$ (Rotation First, Then Scaling)

First, apply the rotation matrix $R$ to vector $x$:

$$
Rx = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} 0(1) + (-1)(2) \\ 1(1) + 0(2) \end{pmatrix} = \begin{pmatrix} -2 \\ 1 \end{pmatrix}
$$

Next, apply the scaling matrix $S$ to the resulting vector:

$$
SRx = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} -2 \\ 1 \end{pmatrix} = \begin{pmatrix} 2(-2) + 0(1) \\ 0(-2) + 1(1) \end{pmatrix} = \begin{pmatrix} -4 \\ 1 \end{pmatrix}
$$

---

Comparison:

RSx = (-2, 2) and SRx = (-4, 1). Since RSx is not equal to SRx, the results are different.

* **Geometric Explanation:** 
  Transformation order matters because matrix multiplication is non-commutative. 
  * In $RSx$, vector $x$ is stretched horizontally first, and then rotated by $90^\circ$ counterclockwise. 
  * In $SRx$, the vector is rotated by $90^\circ$ counterclockwise first, and then the stretching is applied to the already rotated coordinates.

* **Geometric Explanation:** 
  Transformation order matters because matrix multiplication is non-commutative. 
  * In $RSx$, vector $x$ is stretched horizontally first, and then rotated by $90^\circ$ counterclockwise. 
  * In $SRx$, the vector is rotated by $90^\circ$ counterclockwise first, and then the stretching is applied to the already rotated coordinates.
