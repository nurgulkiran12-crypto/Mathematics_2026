# Exercise 7: Identity Matrix, Zero Matrix, and Powers

Let's explore the roles of special matrices like the identity matrix and zero matrix, and see how matrix powers work!

---

Given:

$$
A = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}, \qquad I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}, \qquad 0 = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}
$$

---

## Step 1: Computing $AI$ and $IA$

1. **Multiplying $A$ by $I$ ($AI$):**

$$
AI = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (2 \times 1) + (1 \times 0) & (2 \times 0) + (1 \times 1) \\ (0 \times 1) + (2 \times 0) & (0 \times 0) + (2 \times 1) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}
$$

2. **Multiplying $I$ by $A$ ($IA$):**

$$
IA = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} (1 \times 2) + (0 \times 0) & (1 \times 1) + (0 \times 2) \\ (0 \times 2) + (1 \times 0) & (0 \times 1) + (1 \times 2) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}
$$

---

## Step 2: Computing $A + 0$

Adding the zero matrix to $A$:

$$
A + 0 = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} + \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix} = \begin{pmatrix} 2 + 0 & 1 + 0 \\ 0 + 0 & 2 + 0 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}
$$

---

## Step 3: Computing Powers of $A$ ($A^2$ and $A^3$)

1. **Computing $A^2 = A \times A$:**

$$
A^2 = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} (2 \times 2) + (1 \times 0) & (2 \times 1) + (1 \times 2) \\ (0 \times 2) + (2 \times 0) & (0 \times 1) + (2 \times 2) \end{pmatrix} = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}
$$

2. **Computing $A^3 = A^2 \times A$:**

$$
A^3 = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} (4 \times 2) + (4 \times 0) & (4 \times 1) + (4 \times 2) \\ (0 \times 2) + (4 \times 0) & (0 \times 1) + (4 \times 2) \end{pmatrix} = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}
$$

---

## Step 4: Roles of $I$ and $0$, and Patterns in Powers

* **The Identity Matrix ($I$):** Acts like the number $1$ in matrix multiplication. Multiplying any compatible matrix by $I$ leaves the matrix unchanged ($AI = IA = A$).
* **The Zero Matrix ($0$):** Acts like the number $0$ in matrix addition. Adding it to any matrix leaves the matrix unchanged ($A + 0 = A$).

**Successive Powers of $A$:**

$$
A^1 = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}, \qquad A^2 = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}, \qquad A^3 = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}
$$

**General Pattern ($A^n$):** The diagonal entries are powers of $2$ ($2^n$), and the top-right entry follows the rule $n \cdot 2^{n-1}$. For any positive integer $n$, the general formula is:

$$
A^n = \begin{pmatrix} 2^n & n \cdot 2^{n-1} \\ 0 & 2^n \end{pmatrix}
$$
