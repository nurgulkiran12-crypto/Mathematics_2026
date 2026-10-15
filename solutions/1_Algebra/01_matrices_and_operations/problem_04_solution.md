# Exercise 4: Matrix Multiplication and Noncommutativity

Let's learn how to multiply two matrices together and see why matrix multiplication is non-commutative!

---

## Step 1: Computing the Product $AB$

Given:
$$A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix}$$

Calculating each entry of $AB$:
* **Top-left:** $(1 \times 2) + (2 \times 3) = 2 + 6 = 8$
* **Top-right:** $(1 \times 0) + (2 \times 1) = 0 + 2 = 2$
* **Bottom-left:** $(0 \times 2) + (1 \times 3) = 0 + 3 = 3$
* **Bottom-right:** $(0 \times 0) + (1 \times 1) = 0 + 1 = 1$

Result:
$$AB = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix}$$

---

## Step 2: Computing the Product $BA$

Calculating each entry of $BA$:
* **Top-left:** $(2 \times 1) + (0 \times 0) = 2 + 0 = 2$
* **Top-right:** $(2 \times 2) + (0 \times 1) = 4 + 0 = 4$
* **Bottom-left:** $(3 \times 1) + (1 \times 0) = 3 + 0 = 3$
* **Bottom-right:** $(3 \times 2) + (1 \times 1) = 6 + 1 = 7$

Result:
$$BA = \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}$$

---

## Step 3: Is $AB = BA$?

Comparing our results:
$$AB = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix} \quad \text{and} \quad BA = \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}$$

Clearly, **$AB \neq BA$**, proving that matrix multiplication is **non-commutative**.
