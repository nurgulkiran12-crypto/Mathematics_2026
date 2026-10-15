# Exercise 5: Matrix Times Vector and Linear Combinations

Let's learn two different ways to look at multiplying a matrix by a vector!

---

Given:

$$
A = \begin{pmatrix} 2 & -1 \\ 1 & 3 \end{pmatrix}, \qquad x = \begin{pmatrix} 4 \\ 2 \end{pmatrix}
$$

---

## Step 1: Computing the Product $Ax$

To multiply a matrix by a column vector, you use standard row-by-column multiplication (taking the dot product of each row of $A$ with the vector $x$):

* **Top entry** (Row 1 of $A \times$ vector $x$): 
  $$(2 \times 4) + (-1 \times 2) = 8 - 2 = 6$$

* **Bottom entry** (Row 2 of $A \times$ vector $x$): 
  $$(1 \times 4) + (3 \times 2) = 4 + 6 = 10$$

Result:

$$
Ax = \begin{pmatrix} 6 \\ 10 \end{pmatrix}
$$

---

## Step 2: Expressing $Ax$ as a Linear Combination of Columns

An extremely useful way to think about matrix-vector multiplication is that **multiplying a matrix by a vector takes a linear combination of the matrix's columns**, where the entries of the vector act as the weights (coefficients).

1. Identify the columns of $A$:
   * Column 1: $c_1 = \begin{pmatrix} 2 \\ 1 \end{pmatrix}$
   * Column 2: $c_2 = \begin{pmatrix} -1 \\ 3 \end{pmatrix}$

2. Use the entries of $x$ ($4$ and $2$) as the scalar weights:

$$
Ax = 4 \begin{pmatrix} 2 \\ 1 \end{pmatrix} + 2 \begin{pmatrix} -1 \\ 3 \end{pmatrix}
$$

3. Scale and add them up:

$$
= \begin{pmatrix} 4 \times 2 \\ 4 \times 1 \end{pmatrix} + \begin{pmatrix} 2 \times (-1) \\ 2 \times 3 \end{pmatrix} = \begin{pmatrix} 8 \\ 4 \end{pmatrix} + \begin{pmatrix} -2 \\ 6 \end{pmatrix} = \begin{pmatrix} 8 - 2 \\ 4 + 6 \end{pmatrix} = \begin{pmatrix} 6 \\ 10 \end{pmatrix}
$$

Both methods give the exact same result: **$\begin{pmatrix} 6 \\ 10 \end{pmatrix}$**! This perspective is fundamental in linear algebra because it connects matrix equations directly to column spaces and linear independence.
