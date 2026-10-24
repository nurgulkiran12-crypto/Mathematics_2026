# Exercise 5: Matrix Times Vector

Given:

$$
A = \begin{pmatrix} 2 & -1 \\ 1 & 3 \end{pmatrix}
$$

and 

$$
x = \begin{pmatrix} 4 \\ 2 \end{pmatrix}
$$

---

## Step 1: Computing $Ax$

To compute the matrix-vector product $Ax$ using the standard row-by-column method:

$$
Ax = \begin{pmatrix} 2 & -1 \\ 1 & 3 \end{pmatrix} \begin{pmatrix} 4 \\ 2 \end{pmatrix}
$$

Calculating the entries row by row:

$$
Ax = \begin{pmatrix} (2 \cdot 4) + (-1 \cdot 2) \\ (1 \cdot 4) + (3 \cdot 2) \end{pmatrix}
$$

$$
Ax = \begin{pmatrix} 8 - 2 \\ 4 + 6 \end{pmatrix} = \begin{pmatrix} 6 \\ 10 \end{pmatrix}
$$

---

## Step 2: Linear Combination of the Columns of $A$

Expressing $Ax$ as a linear combination of the columns of $A$ using the entries of $x$ as coefficients:

$$
Ax = 4 \begin{pmatrix} 2 \\ 1 \end{pmatrix} + 2 \begin{pmatrix} -1 \\ 3 \end{pmatrix}
$$

Evaluating the scalar multiplications:

$$
Ax = \begin{pmatrix} 8 \\ 4 \end{pmatrix} + \begin{pmatrix} -2 \\ 6 \end{pmatrix}
$$

Adding the vectors together:

$$
Ax = \begin{pmatrix} 8 - 2 \\ 4 + 6 \end{pmatrix} = \begin{pmatrix} 6 \\ 10 \end{pmatrix}
$$
