# Exercise 6: Transpose and Properties of Transposed Products

Given:

$$
A = \begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{pmatrix}
$$

and

$$
B = \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix}
$$

---

## Step 1: Computing $A^T$ and $B^T$

To find the transpose of a matrix, we swap its rows and columns:

* **For $A$ (size $2 \times 3$), $A^T$ becomes size $3 \times 2$:**

$$
A^T = \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix}
$$

* **For $B$ (size $3 \times 2$), $B^T$ becomes size $2 \times 3$:**

$$
B^T = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \end{pmatrix}
$$

---

## Step 2: Computing $AB$ and Its Transpose $(AB)^T$

First, compute the matrix product $AB$:

$$
AB = \begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix}
$$

$$
AB = \begin{pmatrix} (1 \cdot 1 + 2 \cdot 2 + 3 \cdot -1) & (1 \cdot 0 + 2 \cdot 1 + 3 \cdot 3) \\ (4 \cdot 1 + 5 \cdot 2 + 6 \cdot -1) & (4 \cdot 0 + 5 \cdot 1 + 6 \cdot 3) \end{pmatrix}
$$

$$
AB = \begin{pmatrix} 1 + 4 - 3 & 0 + 2 + 9 \\ 4 + 10 - 6 & 0 + 5 + 18 \end{pmatrix} = \begin{pmatrix} 2 & 11 \\ 8 & 23 \end{pmatrix}
$$

Now, take the transpose of $AB$ to find $(AB)^T$:

$$
(AB)^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}
$$

---

## Step 3: Computing $B^T A^T$ and Verifying the Identity

Next, multiply $B^T$ by $A^T$:

$$
B^T A^T = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \end{pmatrix} \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix}
$$

$$
B^T A^T = \begin{pmatrix} (1 \cdot 1 + 2 \cdot 2 + -1 \cdot 3) & (1 \cdot 4 + 2 \cdot 5 + -1 \cdot 6) \\ (0 \cdot 1 + 1 \cdot 2 + 3 \cdot 3) & (0 \cdot 4 + 1 \cdot 5 + 3 \cdot 6) \end{pmatrix}
$$

$$
B^T A^T = \begin{pmatrix} 1 + 4 - 3 & 4 + 10 - 6 \\ 0 + 2 + 9 & 0 + 5 + 18 \end{pmatrix} = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}
$$

---

## Conclusion

Comparing our results:

$$
(AB)^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix} \quad \text{and} \quad B^T A^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}
$$

Since $(AB)^T = B^T A^T$, the transpose property of matrix products is successfully verified.
