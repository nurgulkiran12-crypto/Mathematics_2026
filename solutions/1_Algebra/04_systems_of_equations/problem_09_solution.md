## Question

Exercise 9. A System from a Sum Condition
Find numbers $x, y$ satisfying:


$$\begin{cases} x + y = 10 \\ 2x + 5y = 32 \end{cases}$$


Solve the system and explain geometrically why the solution is unique.
*(Why this exercise: bridges word problems/sum conditions into linear systems and connects the algebraic solution to the intersection of geometric lines.)*

## Solution

1. **Setting Up the System:**
* We can express the given conditions as a linear system of two equations with two unknowns:

$$\begin{cases} x + y = 10 \\ 2x + 5y = 32 \end{cases}$$


* In matrix form $Ax = b$, this is:

$$\begin{pmatrix} 1 & 1 \\ 2 & 5 \end{pmatrix} \begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 10 \\ 32 \end{pmatrix}$$




2. **Solving the System (via Substitution or Elimination):**
* **Using Substitution:**
* From the first equation, isolate $x$:

$$x = 10 - y$$


* Substitute this into the second equation:

$$2(10 - y) + 5y = 32$$


$$20 - 2y + 5y = 32$$


$$20 + 3y = 32$$


$$3y = 12 \implies y = 4$$


* Now find $x$:

$$x = 10 - 4 = 6$$




* **Solution:** $x = 6$, $y = 4$ (or the point $(6, 4)$).


3. **Checking the Result:**
* Substitute $x = 6$ and $y = 4$ back into the original equations:
* **Equation 1:** $6 + 4 = 10$ (Matches $10$ — Correct)
* **Equation 2:** $2(6) + 5(4) = 12 + 20 = 32$ (Matches $32$ — Correct)




4. **Geometric Explanation of Uniqueness:**
* Each linear equation represents a straight line in the 2D Cartesian plane. Let's rewrite both equations in slope-intercept form ($y = mx + b$):
* Line 1 ($x + y = 10$): $y = -x + 10$ (Slope $m_1 = -1$)
* Line 2 ($2x + 5y = 32$): $5y = -2x + 32 \implies y = -\frac{2}{5}x + \frac{32}{5}$ (Slope $m_2 = -0.4$)


* **Why the solution is unique:** The two lines have **different slopes** ($-1 \neq -0.4$). In a 2D plane, two non-parallel lines are guaranteed to intersect at **one and only one exact point**. Because there is no parallelism or identity between the lines, the intersection point $(6, 4)$ is completely unique.
