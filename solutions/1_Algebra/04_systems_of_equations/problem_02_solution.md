## Question

Exercise 2. Gaussian Elimination — One Solution
Solve using Gaussian elimination:
{ x + y + z = 6, 2x - y + z = 3, x + 2y - z = 2 }
After solving, substitute the result into all equations and check consistency.
*(Why this exercise: demonstrates how to systematically reduce a 3×3 linear system to upper triangular form and solve via back-substitution.)*

## Solution

1. **Setting Up the Augmented Matrix:**
* We write the system as an augmented matrix [A | b]:
[1  1  1 | 6]
[2 -1  1 | 3]
[1  2 -1 | 2]


2. **Applying Gaussian Elimination (Row Operations):**
* **Step 1:** Eliminate entries below the first pivot in column 1.
* $R_2 \leftarrow R_2 - 2R_1$:
[2 - 2(1), -1 - 2(1), 1 - 2(1) | 3 - 2(6)] = [0, -3, -1 | -9]
* $R_3 \leftarrow R_3 - R_1$:
[1 - 1, 2 - 1, -1 - 1 | 2 - 6] = [0, 1, -2 | -4]
* Augmented matrix becomes:
[1  1  1 |  6]
[0 -3 -1 | -9]
[0  1 -2 | -4]


* **Step 2:** Swap rows 2 and 3 to put a convenient pivot ($1$) in the second row, second column ($R_2 \leftrightarrow R_3$):
[1  1  1 |  6]
[0  1 -2 | -4]
[0 -3 -1 | -9]
* **Step 3:** Eliminate the entry below the second pivot by adding 3 times the second row to the third row ($R_3 \leftarrow R_3 + 3R_2$):
* New row 3: [0 + 3(0), -3 + 3(1), -1 + 3(-2) | -9 + 3(-4)] = [0, 0, -7 | -21]
* Augmented matrix becomes (in upper triangular form):
[1  1  1 |   6]
[0  1 -2 |  -4]
[0  0 -7 | -21]


* **Step 4:** Scale the third row to make the pivot 1 ($R_3 \leftarrow (-1/7)R_3$):
* New row 3: [0, 0, 1 | 3]
* Augmented matrix becomes:
[1  1  1 | 6]
[0  1 -2 | -4]
[0  0  1 | 3]




3. **Back-Substitution:**
* From the third row: **$z = 3$**
* From the second row ($y - 2z = -4$):
$y - 2(3) = -4 \implies y - 6 = -4 \implies$ **$y = 2$**
* From the first row ($x + y + z = 6$):
$x + 2 + 3 = 6 \implies x + 5 = 6 \implies$ **$x = 1$**
* **Solution Vector:** x = [1; 2; 3] (meaning $x = 1$, $y = 2$, $z = 3$).


4. **Checking Consistency by Substitution:**
* Substitute $x = 1, y = 2, z = 3$ back into all three original equations:
* **Equation 1:** $1 + 2 + 3 = 6$ (Matches $6$ — Correct)
* **Equation 2:** $2(1) - (2) + (3) = 2 - 2 + 3 = 3$ (Matches $3$ — Correct)
* **Equation 3:** $1 + 2(2) - (3) = 1 + 4 - 3 = 2$ (Matches $2$ — Correct)


* **Conclusion:** The solution satisfies all equations perfectly, confirming the system is consistent and our unique solution is correct.
