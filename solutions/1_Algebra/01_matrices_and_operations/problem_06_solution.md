# Exercise 6: Matrix Transpose and the Transpose Product Property

Let's learn how to find the transpose of a matrix and verify the important property $(AB)^T = B^T A^T$!

---

Given:

$$
A = \begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix}
$$

---

## Step 1: Finding the Transposes ($A^T$ and $B^T$)

The **transpose** of a matrix ($A^T$) is formed by turning its rows into columns (or columns into rows).

1. Transpose of $A$ (swapping $2 \times 3$ to $3 \times 2$):

$$
A^T = \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix}
$$

2. Transpose of $B$ (swapping $3 \times 2$ to $2 \times 3$):

$$
B^T = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \end{pmatrix}
$$

---

## Step 2: Computing the Product $AB$

Matrix $A$ is $2 \times 3$ and $B$ is $3 \times 2$, so their product $AB$ is defined and results in a $2 \times 2$ matrix:

$$
AB = \begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix}
$$

Calculating each entry of $AB$:
* **Top-left:** $(1 \times 1) + (2 \times 2) + (3 \times -1) = 1 + 4 - 3 = 2$
* **Top-right:** $(1 \times 0) + (2 \times 1) + (3 \times 3) = 0 + 2 + 9 = 11$
* **Bottom-left:** $(4 \times 1) + (5 \times 2) + (6 \times -1) = 4 + 10 - 6 = 8$
* **Bottom-right:** $(4 \times 0) + (5 \times 1) + (6 \times 3) = 0 + 5 + 18 = 23$

Result:

$$
AB = \begin{pmatrix} 2 & 11 \\ 8 & 23 \end{pmatrix}
$$

---

## Step 3: Finding $(AB)^T$

Now, take the transpose of our resulting matrix $AB$:

$$
(AB)^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}
$$

---

## Step 4: Computing $B^T A^T$ to Verify the Property

Next, let's compute the product $B^T A^T$ (note that transposition reverses the order of multiplication):

$$
B^T A^T = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \end{pmatrix} \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix}
$$

Calculating each entry of $B^T A^T$:
* **Top-left:** $(1 \times 1) + (2 \times 2) + (-1 \times 3) = 1 + 4 - 3 = 2$
* **Top-right:** $(1 \times 4) + (2 \times 5) + (-1 \times 6) = 4 + 10 - 6 = 8$
* **Bottom-left:** $(0 \times 1) + (1 \times 2) + (3 \times 3) = 0 + 2 + 9 = 11$
* **Bottom-right:** $(0 \times 4) + (1 \times 5) + (3 \times 6) = 0 + 5 + 18 = 23$

Result:

$$
B^T A^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}
$$

---

## Conclusion

Comparing our results:

$$
(AB)^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix} \quad \text{and} \quad B^T A^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}
$$

Since both sides are identical, **$(AB)^T = B^T A^T$** is successfully verified! This rule is a fundamental identity in linear algebra.
