# Exercise 2: Addition, Scalar Multiplication, and Compatibility

Let's break down how to add, subtract, and scale matrices step-by-step!

---

## Step 1: Matrix Addition ($A + B$)

To add two matrices, you simply add the **corresponding entries** (numbers in the exact same position) together. Both $A$ and $B$ are $2 \times 2$ matrices, so they match up perfectly:

$$
A = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix}, \qquad B = \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix}
$$

$$
A + B = 
\begin{pmatrix}
1 + 4 & 2 + (-2) \\
-1 + 0 & 3 + 5
\end{pmatrix} = 
\begin{pmatrix}
5 & 0 \\
-1 & 8
\end{pmatrix}
$$

---

## Step 2: Matrix Subtraction ($A - B$)

Just like addition, matrix subtraction is done entry-by-entry. You subtract each entry in $B$ from its corresponding entry in $A$:

$$
A - B = 
\begin{pmatrix}
1 - 4 & 2 - (-2) \\
-1 - 0 & 3 - 5
\end{pmatrix} = 
\begin{pmatrix}
-3 & 4 \\
-1 & -2
\end{pmatrix}
$$

---

## Step 3: Scalar Multiplication and Combination ($3A - 2B$)

A **scalar** is just a regular number that multiplies every single entry inside the matrix. 

**1. Multiply every entry of $A$ by $3$:**

$$
3A = 3 \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} = \begin{pmatrix} 3 \times 1 & 3 \times 2 \\ 3 \times (-1) & 3 \times 3 \end{pmatrix} = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix}
$$

**2. Multiply every entry of $B$ by $2$:**

$$
2B = 2 \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix} = \begin{pmatrix} 2 \times 4 & 2 \times (-2) \\ 2 \times 0 & 2 \times 5 \end{pmatrix} = \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix}
$$

**3. Subtract the resulting matrices ($3A - 2B$):**

$$
3A - 2B = \begin{pmatrix} 3 - 8 & 6 - (-4) \\ -3 - 0 & 9 - 10 \end{pmatrix} = \begin{pmatrix} -5 & 10 \\ -3 & -1 \end{pmatrix}
$$

---

## Why Matrix Addition Requires the Same Size

Matrix addition and subtraction are performed strictly **entry-by-entry**. Every single number in the first matrix must pair up with a corresponding number in the second matrix. 

If the matrices have different sizes (for example, adding a $2 \times 3$ matrix to a $3 \times 2$ matrix), some numbers in one matrix would be left without a matching partner in the other, making the operation impossible. Therefore, **they must have the exact same dimensions**.
