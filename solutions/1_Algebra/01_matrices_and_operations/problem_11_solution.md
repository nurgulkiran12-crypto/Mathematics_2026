# Exercise 11: When Do Matrices Commute?

Let's find the exact algebraic conditions required for two matrices to commute ($AB = BA$)!

---

Given:

$$
A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} a & b \\ c & d \end{pmatrix}
$$
---

## Step 1: Compute the Product $AB$

Let's multiply matrix $A$ by matrix $B$:

$$
AB = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} a & b \\ c & d \end{pmatrix} = \begin{pmatrix} (1 \cdot a + 1 \cdot c) & (1 \cdot b + 1 \cdot d) \\ (0 \cdot a + 1 \cdot c) & (0 \cdot b + 1 \cdot d) \end{pmatrix}
$$

Result for $AB$:

$$
AB = \begin{pmatrix} a + c & b + d \\ c & d \end{pmatrix}
$$

---

## Step 2: Compute the Product $BA$

Now let's multiply matrix $B$ by matrix $A$ in reverse order:

$$
BA = \begin{pmatrix} a & b \\ c & d \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (a \cdot 1 + b \cdot 0) & (a \cdot 1 + b \cdot 1) \\ (c \cdot 1 + d \cdot 0) & (c \cdot 1 + d \cdot 1) \end{pmatrix}
$$

Result for $BA$:

$$
BA = \begin{pmatrix} a & a + b \\ c & c + d \end{pmatrix}
$$

---

## Step 3: Set $AB = BA$ and Find Conditions

To find when $AB = BA$, we set our two resulting matrices equal to each other entry by entry:

$$
\begin{pmatrix} a + c & b + d \\ c & d \end{pmatrix} = \begin{pmatrix} a & a + b \\ c & c + d \end{pmatrix}
$$

Comparing corresponding entries gives four equations:
1. Top-left: $a + c = a \implies c = 0$
2. Bottom-left: $c = c$ (always true given $c = 0$)
3. Bottom-right: $d = c + d \implies c = 0$ (matches our first condition)
4. Top-right: $b + d = a + b \implies d = a$

---

## Step 4: Describe the General Form of Matrix $B$

From our equations, we found two strict conditions:
* $c = 0$
* $d = a$ ($a$ and $d$ must be equal, while $b$ can be any real number)

Substituting these conditions back into $B$:

$$
B = \begin{pmatrix} a & b \\ 0 & a \end{pmatrix}
$$

**Conclusion:** 
Any matrix $B$ that commutes with $A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$ must have identical diagonal entries ($a = d$) and a zero in the bottom-left position ($c = 0$). They can be written in the general form $\begin{pmatrix} a & b \\ 0 & a \end{pmatrix}$ for any numbers $a$ and $b$
