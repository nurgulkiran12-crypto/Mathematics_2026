# Exercise 15: Associativity of Multiplication and Calculation Paths

Let's verify matrix associativity by comparing two different grouping paths for matrix multiplication!

---

Given:

$$
A = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix}, \qquad C = \begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix}
$$

---

## Step 1: Computing $(AB)C$

**1. Compute $AB$ first:**

$$
AB = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix}
$$

$$
AB = \begin{pmatrix} (1 \cdot 1 + 2 \cdot 2 + 0 \cdot -1) & (1 \cdot 0 + 2 \cdot 1 + 0 \cdot 3) \\ (0 \cdot 1 + 1 \cdot 2 + 1 \cdot -1) & (0 \cdot 0 + 1 \cdot 1 + 1 \cdot 3) \end{pmatrix} = \begin{pmatrix} 5 & 2 \\ 1 & 4 \end{pmatrix}
$$

**2. Multiply by $C$ to find $(AB)C$:**

$$
(AB)C = \begin{pmatrix} 5 & 2 \\ 1 & 4 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix}
$$

$$
(AB)C = \begin{pmatrix} (5 \cdot 2 + 2 \cdot 0) & (5 \cdot 1 + 2 \cdot -1) \\ (1 \cdot 2 + 4 \cdot 0) & (1 \cdot 1 + 4 \cdot -1) \end{pmatrix} = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}
$$

---

## Step 2: Computing $A(BC)$

**1. Compute $BC$ first:**

$$
BC = \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix}
$$
$$
BC = \begin{pmatrix} (1 \cdot 2 + 0 \cdot 0) & (1 \cdot 1 + 0 \cdot -1) \\ (2 \cdot 2 + 1 \cdot 0) & (2 \cdot 1 + 1 \cdot -1) \\ (-1 \cdot 2 + 3 \cdot 0) & (-1 \cdot 1 + 3 \cdot -1) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 4 & 1 \\ -2 & -4 \end{pmatrix}
$$

**2. Multiply by $A$ to find $A(BC)$:**

$$
A(BC) = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 4 & 1 \\ -2 & -4 \end{pmatrix}
$$

$$
A(BC) = \begin{pmatrix} (1 \cdot 2 + 2 \cdot 4 + 0 \cdot -2) & (1 \cdot 1 + 2 \cdot 1 + 0 \cdot -4) \\ (0 \cdot 2 + 1 \cdot 4 + 1 \cdot -2) & (0 \cdot 1 + 1 \cdot 1 + 1 \cdot -4) \end{pmatrix}
$$

$$
A(BC) = \begin{pmatrix} 2 + 8 + 0 & 1 + 2 + 0 \\ 0 + 4 - 2 & 0 + 1 - 4 \end{pmatrix} = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}
$$

---

## Step 3: Comparison and Associativity Explanation

Comparing our results:

$$
(AB)C = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix} \quad \text{and} \quad A(BC) = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}
$$

* **Results:** Both calculation paths yield the exact same matrix, verifying that **$(AB)C = A(BC)$**.
* **Intermediate Operations:** Path 1 computes a $2 \times 3$ by $3 \times 2$ product followed by a $2 \times 2$ product. Path 2 computes a $3 \times 2$ by $2 \times 2$ product followed by a $2 \times 3$ by $3 \times 2$ product. 
* **Meaning of Associativity:** Matrix multiplication is **associative**, meaning the grouping parentheses do not affect the final outcome. This property allows us to write products like $ABC$ unambiguously without parentheses and is vital for optimizing computational efficiency in computer graphics, machine learning, and linear algebra solvers.
