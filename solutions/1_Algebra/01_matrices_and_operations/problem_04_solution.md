# Exercise 4: Matrix Multiplication and Noncommutativity

Let's learn how to multiply two matrices together and see why matrix multiplication behaves differently from regular numbers!

---

## Step 1: Computing the Product $AB$

To multiply two matrices, you take the "dot product" of each **row** of the first matrix with each **column** of the second matrix (multiplying corresponding elements and adding them up).

$$
A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix}
$$

Let's compute $AB$ entry by entry:

**Top-left entry** (Row 1 of $A \times$ Column 1 of $B$):
$$
(1 \times 2) + (2 \times 3) = 2 + 6 = 8
$$

**Top-right entry** (Row 1 of $A \times$ Column 2 of $B$):
$$
(1 \times 0) + (2 \times 1) = 0 + 2 = 2
$$

**Bottom-left entry** (Row 2 of $A \times$ Column 1 of $B$):
$$
(0 \times 2) + (1 \times 3) = 0 + 3 = 3
$$

**Bottom-right entry** (Row 2 of $A \times$ Column 2 of $B$):
$$
(0 \times 0) + (1 \times 1) = 0 + 1 = 1
$$

Putting it together:
$$
AB = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix}
$$

---

## Step 2: Computing the Product $BA$

Now let's reverse the order and multiply $B$ by $A$ ($BA$):

**Top-left entry** (Row 1 of $B \times$ Column 1 of $A$):
$$
(2 \times 1) + (0 \times 0) = 2 + 0 = 2
$$

**Top-right entry** (Row 1 of $B \times$ Column 2 of $A$):
$$
(2 \times 2) + (0 \times 1) = 4 + 0 = 4
$$

**Bottom-left entry** (Row 2 of $B \times$ Column 1 of $A$):
$$
(3 \times 1) + (1 \times 0) = 3 + 0 = 3
$$

**Bottom-right entry** (Row 2 of $B \times$ Column 2 of $A$):
$$
(3 \times 2) + (1 \times 1) = 6 + 1 = 7
$$

Putting it together:
$$
BA = \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}
$$

---

## Step 3: Is $AB = BA$?

Comparing our results:
$$
AB = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix} \quad \text{and} \quad BA = \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}
$$

Clearly, **$AB \neq BA$**. 

---

## What is Noncommutativity?

With regular numbers, multiplication is **commutative**, meaning the order doesn't matter (for example, $2 \times 3 = 3 \times 2 = 6$). 

In linear algebra, **matrix multiplication is generally non-commutative**, meaning changing the order of multiplication ($AB$ versus $BA$) gives completely different results (or might not even be defined due to dimensions). This example proves that the order in which you multiply matrices matters immensely!
