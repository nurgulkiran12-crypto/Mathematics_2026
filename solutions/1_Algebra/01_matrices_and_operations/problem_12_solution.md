# Exercise 12: Formula for a Matrix Power and Induction

Let's compute successive powers of a matrix, find a general pattern, and use algebraic multiplication to prove it holds for any power!

---

Given:

$$
A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}
$$

---

## Step 1: Computing Powers of $A$ ($A^2$, $A^3$, and $A^4$)

1. **Computing $A^2 = A \times A$:**

$$
A^2 = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (1 \cdot 1 + 1 \cdot 0) & (1 \cdot 1 + 1 \cdot 1) \\ (0 \cdot 1 + 1 \cdot 0) & (0 \cdot 1 + 1 \cdot 1) \end{pmatrix} = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}
$$

2. **Computing $A^3 = A^2 \times A$:**

$$
A^3 = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (1 \cdot 1 + 2 \cdot 0) & (1 \cdot 1 + 2 \cdot 1) \\ (0 \cdot 1 + 1 \cdot 0) & (0 \cdot 1 + 1 \cdot 1) \end{pmatrix} = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}
$$

3. **Computing $A^4 = A^3 \times A$:**

$$
A^4 = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (1 \cdot 1 + 3 \cdot 0) & (1 \cdot 1 + 3 \cdot 1) \\ (0 \cdot 1 + 1 \cdot 0) & (0 \cdot 1 + 1 \cdot 1) \end{pmatrix} = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}
$$

---

## Step 2: Formulating the Conjecture for $A^n$

Looking at our computed powers:
* $A^1 = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$
* $A^2 = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}$
* $A^3 = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}$
* $A^4 = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}$

**Conjecture:** For any positive integer $n$, the matrix power $A^n$ is given by:

$$
A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}
$$

---

## Step 3: Proving the Formula for $n + 1$

To prove this pattern holds universally, assume the formula is true for some arbitrary power $n$. We want to find $A^{n+1}$ by multiplying $A^n$ by $A$:

$$
A^{n+1} = A^n \cdot A
$$

Substitute our formula for $A^n$ and matrix $A$:

$$
A^{n+1} = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}
$$

Now, multiply the two matrices:

$$
A^{n+1} = \begin{pmatrix} (1 \cdot 1 + n \cdot 0) & (1 \cdot 1 + n \cdot 1) \\ (0 \cdot 1 + 1 \cdot 0) & (0 \cdot 1 + 1 \cdot 1) \end{pmatrix}
$$

Simplify the entries:

$$
A^{n+1} = \begin{pmatrix} 1 & 1 + n \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1 & n + 1 \\ 0 & 1 \end{pmatrix}
$$

**Conclusion:** 
Multiplying the formula for $n$ by $A$ yields exactly the formula with $n$ replaced by $n+1$. This confirms that our conjecture is mathematically sound and holds true for all positive integers $n$.
