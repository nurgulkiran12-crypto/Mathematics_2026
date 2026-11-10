## Question

Exercise 5. Row Echelon Form and Number of Solutions
For the augmented matrix:
[1  2 -1 | 3]
[0  1  2 | 1]
[0  0  0 | 0]
determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.

## Solution

1. **Analyzing the Augmented Matrix:**
* The matrix is already in row-echelon form. Let's translate the rows back into linear equations, assuming our variables are $x$, $y$, and $z$:
* **Row 1:** $1x + 2y - z = 3$ (Pivot variable: $x$)
* **Row 2:** $0x + 1y + 2z = 1$ (Pivot variable: $y$)
* **Row 3:** $0x + 0y + 0z = 0$ (trivial identity, no contradiction)




2. **Determining Free Variables and Number of Solutions:**
* **Number of variables ($n$):** 3 ($x, y, z$).
* **Rank of coefficient matrix ($r$):** 2 (since there are 2 non-zero rows with leading pivots).
* **Free variables:** The number of free variables is given by $n - r = 3 - 2 = 1$. Because there is 1 free variable and no contradictory rows (like $0 = c$ where $c \neq 0$), the system is consistent and has **infinitely many solutions**.


3. **Writing the Solution in Parametric Form:**
* Let the free variable $z$ be our parameter: let **$z = t$**, where $t$ is any real number.
* From Row 2 ($y + 2z = 1$):
$y + 2t = 1 \implies$ **$y = 1 - 2t$**
* From Row 1 ($x + 2y - z = 3$):
$x + 2(1 - 2t) - t = 3$
$x + 2 - 4t - t = 3 \implies x - 5t + 2 = 3 \implies$ **$x = 1 + 5t$**
* **Parametric Solution:**
* $x = 1 + 5t$
* $y = 1 - 2t$
* $z = t$




4. **Checking the Solution:**
* Let's test a sample parameter value, such as $t = 1$:
* Point: $(6, -1, 1)$
* Substitute into Row 1: $6 + 2(-1) - (1) = 6 - 2 - 1 = 3$ (Matches)
* Substitute into Row 2: $(-1) + 2(1) = -1 + 2 = 1$ (Matches)


* The solution family satisfies all rows of the matrix perfectly.
