# Exercise 9: Composing Transformations

Let's explore how matrix multiplication represents the composition of geometric transformations and why the order in which we apply them matters!

---

Given:

$$
S = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix}, \qquad R = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}, \qquad x = \begin{pmatrix} 1 \\ 2 \end{pmatrix}
$$

---

## Step 1: Computing $RSx$ (Scaling First, then Rotating)

To compute $RSx$, we can either compute the product matrix $RS$ first or apply the matrices to $x$ from right to left ($S$ acts on $x$ first, then $R$ acts on the result):

1. **Apply $S$ to $x$ ($Sx$):**

$$
Sx = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} (2 \times 1) + (0 \times 2) \\ (0 \times 1) + (1 \times 2) \end{pmatrix} = \begin{pmatrix} 2 \\ 2 \end{pmatrix}
$$

2. **Apply $R$ to the result ($RSx$):**

$$
RSx = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 2 \\ 2 \end{pmatrix} = \begin{pmatrix} (0 \times 2) + (-1 \times 2) \\ (1 \times 2) + (0 \times 2) \end{pmatrix} = \begin{pmatrix} -2 \\ 2 \end{pmatrix}
$$

---

## Step 2: Computing $SRx$ (Rotating First, then Scaling)

To compute $SRx$, we apply $R$ to $x$ first, and then apply $S$ to the result:

1. **Apply $R$ to $x$ ($Rx$):**

$$
Rx = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} (0 \times 1) + (-1 \times 2) \\ (1 \times 1) + (0 \times 2) \end{pmatrix} = \begin{pmatrix} -2 \\ 1 \end{pmatrix}
$$

2. **Apply $S$ to the result ($SRx$):**

$$
SRx = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} -2 \\ 1 \end{pmatrix} = \begin{pmatrix} (2 \times -2) + (0 \times 1) \\ (0 \times -2) + (1 \times 1) \end{pmatrix} = \begin{pmatrix} -4 \\ 1 \end{pmatrix}
$$

---

## Step 3: Comparison and Geometric Explanation

Comparing our results:

$$
RSx = \begin{pmatrix} -2 \\ 2 \end{pmatrix} \quad \text{and} \quad SRx = \begin{pmatrix} -4 \\ 1 \end{pmatrix}
$$

Since $RSx \neq SRx$, the order of operations changes the final position of the vector. 

* **Why order matters geometrically:** Matrix multiplication corresponds to composing geometric transformations. When you scale an object first (stretching it horizontally along the x-axis) and *then* rotate it, the stretched coordinates get rotated to a new position. However, if you rotate the object *first* and then stretch it, the stretching happens along the original axes relative to the already-rotated position. 
* Because geometric transformations are generally **non-commutative**, doing operation $A$ then $B$ is not the same as doing $B$ then $A$, which is why matrix multiplication is non-commutative!
