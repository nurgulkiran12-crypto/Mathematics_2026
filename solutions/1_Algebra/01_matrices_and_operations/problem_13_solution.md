# Exercise 13: A Recurrence Written in Matrix Form

Let's explore how matrix powers generate the Fibonacci sequence and how matrix multiplication performs a recurrence step!

---

Given:

$$
F = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}
$$

---

## Step 1: Computing Powers of $F$ ($F^2$, $F^3$, $F^4$, and $F^5$)

**1. Computing $F^2 = F \times F$:**

$$
F^2 = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} (1 \cdot 1 + 1 \cdot 1) & (1 \cdot 1 + 1 \cdot 0) \\ (1 \cdot 1 + 0 \cdot 1) & (1 \cdot 1 + 0 \cdot 0) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}
$$

**2. Computing $F^3 = F^2 \times F$:**

$$
F^3 = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} (2 \cdot 1 + 1 \cdot 1) & (2 \cdot 1 + 1 \cdot 0) \\ (1 \cdot 1 + 1 \cdot 1) & (1 \cdot 1 + 1 \cdot 0) \end{pmatrix} = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}
$$

**3. Computing $F^4 = F^3 \times F$:**

$$
F^4 = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} (3 \cdot 1 + 2 \cdot 1) & (3 \cdot 1 + 2 \cdot 0) \\ (2 \cdot 1 + 1 \cdot 1) & (2 \cdot 1 + 1 \cdot 0) \end{pmatrix} = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix}
$$

**4. Computing $F^5 = F^4 \times F$:**

$$
F^5 = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} (5 \cdot 1 + 3 \cdot 1) & (5 \cdot 1 + 3 \cdot 0) \\ (3 \cdot 1 + 2 \cdot 1) & (3 \cdot 1 + 2 \cdot 0) \end{pmatrix} = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}
$$

---

## Step 2: Relationship with the Fibonacci Sequence

Comparing the entries of our matrix powers with the Fibonacci sequence ($0, 1, 1, 2, 3, 5, 8, \dots$):

$F^1$ is $\begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}$

$F^2$ is $\begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}$

$F^3$ is $\begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}$

$F^4$ is $\begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix}$

$F^5$ is $\begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}$

**Observation:** Every entry in $F^n$ is a Fibonacci number! Specifically, the matrix power follows the general form:

$$
F^n = \begin{pmatrix} F_{n+1} & F_n \\ F_n & F_{n-1} \end{pmatrix}
$$

---

## Step 3: Performing a Recurrence Step

Now let's multiply $F$ by a general vector $\begin{pmatrix} a \\ b \end{pmatrix}$:

$$
F \begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} (1 \cdot a + 1 \cdot b) \\ (1 \cdot a + 0 \cdot b) \end{pmatrix} = \begin{pmatrix} a + b \\ a \end{pmatrix}
$$

**Explanation:** This multiplication performs a single step of a recurrence relation. The new top term becomes the sum of the two previous terms ($a + b$), and the new bottom term keeps the previous top term ($a$) ready to step into the next iteration.
