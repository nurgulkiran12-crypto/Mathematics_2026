# Exercise 8: Row Operations and Their Reversibility

Given:

$$
A = \begin{pmatrix} 1 & 2 & -1 \\ 2 & 4 & 1 \\ -1 & 1 & 3 \end{pmatrix}
$$

---

## Step 1: Performing $R_2 \leftarrow R_2 - 2R_1$

Subtract 2 times Row 1 from Row 2:

$$
\begin{pmatrix} 1 & 2 & -1 \\ 2 - 2(1) & 4 - 2(2) & 1 - 2(-1) \\ -1 & 1 & 3 \end{pmatrix}
$$

$$
=
$$

$$
\begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ -1 & 1 & 3 \end{pmatrix}
$$

* **Reversing operation:** $R_2 \leftarrow R_2 + 2R_1$

---

## Step 2: Performing $R_3 \leftarrow R_3 + R_1$

Add Row 1 to Row 3:

$$
\begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ -1 + 1 & 1 + 2 & 3 + (-1) \end{pmatrix}
$$

$$
=
$$

$$
\begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ 0 & 3 & 2 \end{pmatrix}
$$

* **Reversing operation:** $R_3 \leftarrow R_3 - R_1$

---

## Step 3: Interchange $R_2$ and $R_3$

Swap Row 2 and Row 3:

$$
\begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 2 \\ 0 & 0 & 3 \end{pmatrix}
$$

* **Reversing operation:** Interchange $R_2$ and $R_3$ again.
