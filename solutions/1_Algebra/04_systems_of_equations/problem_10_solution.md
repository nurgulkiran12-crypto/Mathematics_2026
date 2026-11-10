## Question

Exercise 10. A Polynomial Through Three Points
Find a polynomial $p(x) = ax^2 + bx + c$ whose graph passes through $(0, 1)$, $(1, 3)$, and $(2, 9)$. Reduce the problem to a system of equations and check the result by substituting all three points.
*(Why this exercise: demonstrates how curve-fitting and polynomial interpolation can be modeled and solved using linear systems of equations.)*

## Solution

1. **Setting Up the System of Equations:**
* We are given the general quadratic form $p(x) = ax^2 + bx + c$ and three points $(x, y)$ that must lie on its graph. Substitute each point into the equation:
* For $(0, 1)$:

$$a(0)^2 + b(0) + c = 1 \implies c = 1$$


* For $(1, 3)$:

$$a(1)^2 + b(1) + c = 3 \implies a + b + c = 3$$


* For $(2, 9)$:

$$a(2)^2 + b(2) + c = 9 \implies 4a + 2b + c = 9$$






2. **Writing the System in Matrix Form:**
* Substituting $c = 1$ into the second and third equations gives a $2 \times 2$ system for $a$ and $b$:

$$\begin{cases} a + b + 1 = 3 \\ 4a + 2b + 1 = 9 \end{cases} \implies \begin{cases} a + b = 2 \\ 4a + 2b = 8 \end{cases}$$


* In matrix form $Ax = b$, this can be expressed as:

$$\begin{pmatrix} 0^2 & 0 & 1 \\ 1^2 & 1 & 1 \\ 2^2 & 2 & 1 \end{pmatrix} \begin{pmatrix} a \\ b \\ c \end{pmatrix} = \begin{pmatrix} 1 \\ 3 \\ 9 \end{pmatrix} \implies \begin{pmatrix} 0 & 0 & 1 \\ 1 & 1 & 1 \\ 4 & 2 & 1 \end{pmatrix} \begin{pmatrix} a \\ b \\ c \end{pmatrix} = \begin{pmatrix} 1 \\ 3 \\ 9 \end{pmatrix}$$




3. **Solving the System:**
* From the first equation, we immediately know **$c = 1$**.
* Simplify the remaining two equations:
* Equation 2: $a + b = 2 \implies b = 2 - a$
* Equation 3: $4a + 2b = 8$ (dividing by 2 gives $2a + b = 4$)


* Substitute $b = 2 - a$ into $2a + b = 4$:

$$2a + (2 - a) = 4 \implies a + 2 = 4 \implies$$



**$a = 2$**
* Now find $b$:

$$b = 2 - 2 \implies$$



**$b = 0$**
* **Result:** $a = 2, b = 0, c = 1$, yielding the polynomial:

$$p(x) = 2x^2 + 1$$




4. **Checking the Result by Substitution:**
* Test all three points in $p(x) = 2x^2 + 1$:
* **Point $(0, 1)$:** $p(0) = 2(0)^2 + 1 = 0 + 1 = 1$ (Matches $1$ — Correct)
* **Point $(1, 3)$:** $p(1) = 2(1)^2 + 1 = 2(1) + 1 = 3$ (Matches $3$ — Correct)
* **Point $(2, 9)$:** $p(2) = 2(2)^2 + 1 = 2(4) + 1 = 8 + 1 = 9$ (Matches $9$ — Correct)


* **Conclusion:** The polynomial $p(x) = 2x^2 + 1$ satisfies all conditions perfectly.
