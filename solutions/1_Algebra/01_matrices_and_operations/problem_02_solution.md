# Exercise 2: Addition, Scalar Multiplication, and Compatibility

Let's break down how to add, subtract, and scale matrices step-by-step!

---

Given:

$$
A = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix}, \qquad B = \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix}
$$

---

## Step 1: Matrix Addition ($A + B$)

To add two matrices, we add their corresponding entries element-by-element:

$$
A + B = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} + \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix}
$$

$$
A + B = \begin{pmatrix} 1 + 4 & 2 + (-2) \\ -1 + 0 & 3 + 5 \end{pmatrix} = \begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix}
$$

---

## Step 2: Matrix Subtraction ($A - B$)

To subtract two matrices, we subtract the corresponding entries element-by-element:

$$
A - B = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} - \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix}
$$

$$
A - B = \begin{pmatrix} 1 - 4 & 2 - (-2) \\ -1 - 0 & 3 - 5 \end{pmatrix} = \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix}
$$

---

## Step 3: Scalar Multiplication ($3A - 2B$)

First, multiply each matrix by its scalar factor:

$$
3A = 3 \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix}
$$

$$
2B = 2 \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix} = \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix}
$$

Now, subtract the resulting matrices:

$$
3A - 2B = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix} - \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix} = \begin{pmatrix} 3 - 8 & 6 - (-4) \\ -3 - 0 & 9 - 10 \end{pmatrix} = \begin{pmatrix} -5 & 10 \\ -3 & -1 \end{pmatrix}
$$

---

## Step 4: Why Matrix Addition Requires the Same Size

Matrix addition and subtraction are performed strictly **entry-by-entry**. Every single number in the first matrix must pair up with a corresponding position in the second matrix. If the dimensions (sizes) do not match, some entries will lack a pairing partner, making addition or subtraction undefined.
