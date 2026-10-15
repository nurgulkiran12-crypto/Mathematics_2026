# Exercise 8: Row Operations and Their Reversibility

Let's perform elementary row operations step-by-step and see how each one can be completely reversed!

---

Given initial matrix $A$:

$$
A = \begin{pmatrix} 1 & 2 & -1 \\ 2 & 4 & 1 \\ -1 & 1 & 3 \end{pmatrix}
$$

---

## Step 1: Perform $R_2 \leftarrow R_2 - 2R_1$

We subtract $2$ times Row 1 from Row 2 (leaving Rows 1 and 3 unchanged):
* **New Row 2:** $(2 - 2(1), 4 - 2(2), 1 - 2(-1)) = (2 - 2, 4 - 4, 1 - (-2)) = (0, 0, 3)$

Matrix after Step 1:

$$
\begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ -1 & 1 & 3 \end{pmatrix}
$$

* **Reversing Operation 1:** To undo subtracting $2$ times Row 1 from Row 2, we add $2$ times Row 1 back: **$R_2 \leftarrow R_2 + 2R_1$**.

---

## Step 2: Perform $R_3 \leftarrow R_3 + R_1$

We add Row 1 to Row 3 (using the matrix from Step 1, leaving Rows 1 and 2 unchanged):
* **New Row 3:** $(-1 + 1, 1 + 2, 3 + (-1)) = (0, 3, 2)$

Matrix after Step 2:

$$
\begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ 0 & 3 & 2 \end{pmatrix}
$$

* **Reversing Operation 2:** To undo adding Row 1 to Row 3, we subtract Row 1: **$R_3 \leftarrow R_3 - R_1$**.

---

## Step 3: Interchange $R_2$ and $R_3$

We swap Row 2 and Row 3 (using the matrix from Step 2):
* Row 2 becomes $(0, 3, 2)$
* Row 3 becomes $(0, 0, 3)$

Matrix after Step 3:

$$
\begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 2 \\ 0 & 0 & 3 \end{pmatrix}
$$

* **Reversing Operation 3:** To undo swapping two rows, we simply swap them back: **interchange $R_2$ and $R_3$ again**.

---

## Summary of Reversing Operations

1. **Operation 1 ($R_2 \leftarrow R_2 - 2R_1$):** Reversed by **$R_2 \leftarrow R_2 + 2R_1$**
2. **Operation 2 ($R_3 \leftarrow R_3 + R_1$):** Reversed by **$R_3 \leftarrow R_3 - R_1$**
3. **Operation 3 (Interchange $R_2$ and $R_3$):** Reversed by **interchanging $R_2$ and $R_3$ again**

This reversibility is what makes elementary row operations so powerful in Gaussian elimination and finding matrix inverses!
