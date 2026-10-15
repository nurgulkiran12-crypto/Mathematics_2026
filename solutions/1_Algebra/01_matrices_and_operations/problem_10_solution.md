# Exercise 10: Columns of a Matrix Product

Let's explore how a matrix-matrix product can be broken down column by column using matrix-vector multiplication!

---

Given:

$$
A = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & 2 \\ -1 & 0 \\ 3 & 1 \end{pmatrix}
$$
Let the columns of $B$ be $b_1 = \begin{pmatrix} 1 \\ -1 \\ 3 \end{pmatrix}$ and $b_2 = \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix}$.

---

## Step 1: Computing $Ab_1$ and $Ab_2$

1. **Computing $Ab_1$:**

$$
Ab_1 = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ -1 \\ 3 \end{pmatrix} = \begin{pmatrix} (1 \times 1) + (2 \times -1) + (0 \times 3) \\ (0 \times 1) + (1 \times -1) + (1 \times 3) \end{pmatrix} = \begin{pmatrix} 1 - 2 + 0 \\ 0 - 1 + 3 \end{pmatrix} = \begin{pmatrix} -1 \\ 2 \end{pmatrix}
$$

2. **Computing $Ab_2$:**

$$
Ab_2 = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix} = \begin{pmatrix} (1 \times 2) + (2 \times 0) + (0 \times 1) \\ (0 \times 2) + (1 \times 0) + (1 \times 1) \end{pmatrix} = \begin{pmatrix} 2 + 0 + 0 \\ 0 + 0 + 1 \end{pmatrix} = \begin{pmatrix} 2 \\ 1 \end{pmatrix}
$$

---

## Step 2: Computing the Matrix Product $AB$

Now let's compute the full matrix product $AB$ using standard row-by-column multiplication:

$$
AB = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 2 \\ -1 & 0 \\ 3 & 1 \end{pmatrix}
$$

Calculating each entry:
* **Top-left:** $(1 \times 1) + (2 \times -1) + (0 \times 3) = 1 - 2 + 0 = -1$
* **Top-right:** $(1 \times 2) + (2 \times 0) + (0 \times 1) = 2 + 0 + 0 = 2$
* **Bottom-left:** $(0 \times 1) + (1 \times -1) + (1 \times 3) = 0 - 1 + 3 = 2$
* **Bottom-right:** $(0 \times 2) + (1 \times 0) + (1 \times 1) = 0 + 0 + 1 = 1$

Result:

$$
AB = \begin{pmatrix} -1 & 2 \\ 2 & 1 \end{pmatrix}
$$

---

## Step 3: Comparison and Explanation

Comparing our results:
* $Ab_1 = \begin{pmatrix} -1 \\ 2 \end{pmatrix}$ (this is the first column of $AB$)
* $Ab_2 = \begin{pmatrix} 2 \\ 1 \end{pmatrix}$ (this is the second column of $AB$)
* $AB = \begin{pmatrix} -1 & 2 \\ 2 & 1 \end{pmatrix}$

**Why the columns of $AB$ are $Ab_1$ and $Ab_2$:**
When you multiply a matrix $A$ by another matrix $B = \begin{pmatrix} b_1 & b_2 & \dots & b_n \end{pmatrix}$, matrix multiplication is defined such that each column of the resulting product is formed by multiplying $A$ by the corresponding column vector of $B$. Therefore, $AB = \begin{pmatrix} Ab_1 & Ab_2 & \dots & Ab_n \end{pmatrix}$. This gives us a powerful perspective: multiplying two matrices is just repeatedly multiplying the first matrix by each column vector of the second matrix!
