# Exercise 11: When Do Matrices Commute?

Given:
$$
A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} a & b \\ c & d \end{pmatrix}
$$

---

## Step 1: Computing $AB$ and $BA$

* **Computing $AB$:**
  $$
  AB = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} a & b \\ c & d \end{pmatrix} = \begin{pmatrix} a+c & b+d \\ c & d \end{pmatrix}
  $$

* **Computing $BA$:**
  $$
  BA = \begin{pmatrix} a & b \\ c & d \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} a & a+b \\ c & c+d \end{pmatrix}
  $$

---

## Step 2: Finding Conditions for $AB = BA$

Equating the corresponding entries of $AB$ and $BA$:
1. $a + c = a \implies c = 0$
2. $b + d = a + b \implies d = a$
3. $c = c$ (satisfied since $c = 0$)
4. $d = c + d \implies c = 0$ (consistent)

Thus, the conditions are **$c = 0$** and **$d = a$**, while $a$ and $b$ can be any real numbers.

---

## Step 3: General Form of Matrix $B$

Substituting these conditions into $B$, the general form of all matrices that commute with $A$ is:
$$
B = \begin{pmatrix} a & b \\ 0 & a \end{pmatrix}
$$
where $a$ and $b$ are arbitrary scalars.
