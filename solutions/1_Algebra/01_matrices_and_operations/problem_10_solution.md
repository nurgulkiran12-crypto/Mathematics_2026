# Exercise 10: Columns of a Matrix Product

Given:
$$
A = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & 2 \\ -1 & 0 \\ 3 & 1 \end{pmatrix}
$$
Columns of $B$: $b_1 = \begin{pmatrix} 1 \\ -1 \\ 3 \end{pmatrix}$, $b_2 = \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix}$.

---

## 1. Computing $Ab_1$ and $Ab_2$

* **$Ab_1$:**
  $$
  Ab_1 = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ -1 \\ 3 \end{pmatrix} = \begin{pmatrix} -1 \\ 2 \end{pmatrix}
  $$

* **$Ab_2$:**
  $$
  Ab_2 = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix} = \begin{pmatrix} 2 \\ 1 \end{pmatrix}
  $$

---

## 2. Computing $AB$

$$
AB = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 2 \\ -1 & 0 \\ 3 & 1 \end{pmatrix} = \begin{pmatrix} -1 & 2 \\ 2 & 1 \end{pmatrix}
$$

---

## 3. Comparison and Explanation

* **Comparison:** 
  The columns of $AB$ are $\begin{pmatrix} -1 \\ 2 \end{pmatrix}$ and $\begin{pmatrix} 2 \\ 1 \end{pmatrix}$, which are identical to $Ab_1$ and $Ab_2$.

* **Explanation:** 
  By definition, the columns of a product matrix $AB$ are formed by multiplying $A$ by each column of $B$ ($AB = \begin{pmatrix} Ab_1 & Ab_2 \end{pmatrix}$).
