# Method 1: Standard Row-Column Multiplication for $Ax$

Given:

$$
A = \begin{pmatrix} 2 & -1 \\ 1 & 3 \end{pmatrix}, \qquad x = \begin{pmatrix} 4 \\ 2 \end{pmatrix}
$$

To compute the matrix-vector product $Ax$ using the standard row-by-column method, we multiply the entries of each row of $A$ by the corresponding entries of vector $x$ and sum them up.

**Top entry (Row 1 of $A$ multiplied by $x$):**

$$
(2 \cdot 4) + (-1 \cdot 2) = 8 - 2 = 6
$$

**Bottom entry (Row 2 of $A$ multiplied by $x$):**

$$
(1 \cdot 4) + (3 \cdot 2) = 4 + 6 = 10
$$

Putting the entries together into the resulting vector:

$$
Ax = \begin{pmatrix} 6 \\ 10 \end{pmatrix}
$$
