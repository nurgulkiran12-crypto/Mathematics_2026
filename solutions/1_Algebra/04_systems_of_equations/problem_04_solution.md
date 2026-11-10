## Question

Exercise 4. Infinitely Many Solutions
Solve:
{ x + y + z = 2, 2x + 2y + 2z = 4, x - y + z = 0 }
Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.

## Solution

1. **Setting Up the Augmented Matrix:**
* Write the system as an augmented matrix [A | b]:
[1  1  1 | 2]
[2  2  2 | 4]
[1 -1  1 | 0]


2. **Applying Gaussian Elimination:**
* **Step 1:** Eliminate the entry below the first pivot in row 2 by subtracting 2 times the first row ($R_2 \leftarrow R_2 - 2R_1$):
* New row 2: [2 - 2(1), 2 - 2(1), 2 - 2(1) | 4 - 2(2)] = [0, 0, 0 | 0]


* **Step 2:** Eliminate the entry below the first pivot in row 3 by subtracting the first row ($R_3 \leftarrow R_3 - R_1$):
* New row 3: [1 - 1, -1 - 1, 1 - 1 | 0 - 2] = [0, -2, 0 | -2]


* The augmented matrix becomes:
[1  1  1 |  2]
[0  0  0 |  0]
[0 -2  0 | -2]
* **Step 3:** Swap rows 2 and 3 to place the non-zero row in the second position ($R_2 \leftrightarrow R_3$):
[1  1  1 |  2]
[0 -2  0 | -2]
[0  0  0 |  0]
* **Step 4:** Scale the second row to make the leading coefficient 1 ($R_2 \leftarrow (-1/2)R_2$):
* New row 2: [0, 1, 0 | 1]
* Final row-echelon matrix:
[1  1  1 | 2]
[0  1  0 | 1]
[0  0  0 | 0]




3. **Interpreting and Writing the Solution in Parametric Form:**
* Converting the non-zero rows back into equations:
* Row 2 gives: $y = 1$
* Row 1 gives: $x + y + z = 2$


* Since column 3 has no pivot, variable **$z$ is a free variable**. Let $z = t$, where $t$ is any real number parameter.
* Substitute $y = 1$ and $z = t$ into the first equation:
$x + 1 + t = 2 \implies x = 1 - t$
* **Parametric Solution:**
* $x = 1 - t$
* $y = 1$
* $z = t$
*(Or in vector form: $(x, y, z) = (1, 1, 0) + t(-1, 0, 1)$)*




4. **Checking a Specific Parameter Value:**
* Let us choose parameter $t = 2$. This gives the point:
* $x = 1 - 2 = -1$
* $y = 1$
* $z = 2$
* Point: $(-1, 1, 2)$


* Substitute this point back into all three original equations:
* **Equation 1:** $(-1) + 1 + 2 = 2$ (Matches $2$ — Correct)
* **Equation 2:** $2(-1) + 2(1) + 2(2) = -2 + 2 + 4 = 4$ (Matches $4$ — Correct)
* **Equation 3:** $(-1) - (1) + 2 = -2 + 2 = 0$ (Matches $0$ — Correct)


* **Conclusion:** The generated point satisfies all equations, verifying that our parametric solution family is correct.
