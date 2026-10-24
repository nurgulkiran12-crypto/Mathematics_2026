# Exercise 4: Matrix Multiplication and Noncommutativity

Given:

$$
A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix}
$$

## 1. Computing $AB$
$$
AB = \begin{pmatrix} (1 \cdot 2 + 2 \cdot 3) & (1 \cdot 0 + 2 \cdot 1) \\ (0 \cdot 2 + 1 \cdot 3) & (0 \cdot 0 + 1 \cdot 1) \end{pmatrix} = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix}
$$

## 2. Computing $BA$
$$
BA = \begin{pmatrix} (2 \cdot 1 + 0 \cdot 0) & (2 \cdot 2 + 0 \cdot 1) \\ (3 \cdot 1 + 1 \cdot 0) & (3 \cdot 2 + 1 \cdot 1) \end{pmatrix} = \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}
$$

## 3. Conclusion
Since $AB \neq BA$, matrix multiplication is **non-commutative**. The order of multiplication changes the result.
