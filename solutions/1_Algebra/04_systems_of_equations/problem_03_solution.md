## Question

Exercise 3. Inconsistent System
Solve or show that the system is inconsistent:
{ x + 2y = 3, 2x + 4y = 7 }
Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.
*(Why this exercise: demonstrates how Gaussian elimination identifies inconsistent systems with no solutions through contradictory row results.)*

## Solution

1. **Setting Up the Augmented Matrix:**## Question

Exercise 3. Inconsistent System
Solve or show that the system is inconsistent:
{ x + 2y = 3, 2x + 4y = 7 }
Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.
*(Why this exercise: demonstrates how Gaussian elimination identifies inconsistent systems with no solutions through contradictory row results.)*

## Solution

1. **Setting Up the Augmented Matrix:**
* We write the linear system as an augmented matrix [A | b]:
[1  2 | 3]
[2  4 | 7]


2. **Applying Gaussian Elimination:**
* **Step 1:** Eliminate the leading entry in the second row by subtracting 2 times the first row from the second row ($R_2 \leftarrow R_2 - 2R_1$):
* New row 2: [2 - 2(1), 4 - 2(2) | 7 - 2(3)] = [0, 0 | 7 - 6] = [0, 0 | 1]
* Augmented matrix becomes:
[1  2 | 3]
[0  0 | 1]




3. **Interpreting the Contradiction in Terms of Equations:**
* Converting the final row back into equation form:
$0x + 0y = 1 \implies 0 = 1$
* This statement is an impossible mathematical contradiction. Because no combination of $x$ and $y$ can ever satisfy $0 = 1$, the system has **no solution** and is classified as **inconsistent**.
* **Geometric Interpretation:** If you rearrange both equations into slope-intercept form ($y = -\frac{1}{2}x + \frac{3}{2}$ and $y = -\frac{1}{2}x + \frac{7}{4}$), you can see that they represent two distinct **parallel lines** with identical slopes but different y-intercepts. Because parallel lines never cross, they share no points of intersection, which matches our algebraic conclusion.
* We write the linear system as an augmented matrix [A | b]:
[1  2 | 3]
[2  4 | 7]


2. **Applying Gaussian Elimination:**
* **Step 1:** Eliminate the leading entry in the second row by subtracting 2 times the first row from the second row ($R_2 \leftarrow R_2 - 2R_1$):
* New row 2: [2 - 2(1), 4 - 2(2) | 7 - 2(3)] = [0, 0 | 7 - 6] = [0, 0 | 1]
* Augmented matrix becomes:
[1  2 | 3]
[0  0 | 1]




3. **Interpreting the Contradiction in Terms of Equations:**
* Converting the final row back into equation form:
$0x + 0y = 1 \implies 0 = 1$
* This statement is an impossible mathematical contradiction. Because no combination of $x$ and $y$ can ever satisfy $0 = 1$, the system has **no solution** and is classified as **inconsistent**.
* **Geometric Interpretation:** If you rearrange both equations into slope-intercept form ($y = -\frac{1}{2}x + \frac{3}{2}$ and $y = -\frac{1}{2}x + \frac{7}{4}$), you can see that they represent two distinct **parallel lines** with identical slopes but different y-intercepts. Because parallel lines never cross, they share no points of intersection, which matches our algebraic conclusion.
