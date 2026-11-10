## Question

Exercise 5. A 3×3 Matrix
Use Gauss-Jordan elimination to find the inverse of:
A = [1 1 0; 0 1 1; 1 0 1]
Check the result by multiplication.

## Solution

1. **Setting Up the Augmented Matrix:**
* We combine our 3 × 3 matrix $A$ with the 3 × 3 identity matrix $I$ to form the augmented matrix [A | I]:
[1 1 0 | 1 0 0]
[0 1 1 | 0 1 0]
[1 0 1 | 0 0 1]


2. **Performing Gauss-Jordan Row Operations:**
* **Step 1:** Eliminate the leading entry in the third row by subtracting the first row from the third row ($R_3 \leftarrow R_3 - R_1$):
* New row 3: [1 - 1, 0 - 1, 1 - 0 | 0 - 1, 0 - 0, 1 - 0] = [0, -1, 1 | -1, 0, 1]
* Augmented matrix becomes:
[1  1  0 |  1  0  0]
[0  1  1 |  0  1  0]
[0 -1  1 | -1  0  1]


* **Step 2:** Eliminate the entry below the second pivot by adding the second row to the third row ($R_3 \leftarrow R_3 + R_2$):
* New row 3: [0 + 0, -1 + 1, 1 + 1 | -1 + 0, 0 + 1, 1 + 0] = [0, 0, 2 | -1, 1, 1]
* Augmented matrix becomes:
[1 1 0 |  1  0  0]
[0 1 1 |  0  1  0]
[0 0 2 | -1  1  1]


* **Step 3:** Scale the third row to make the pivot equal to 1 ($R_3 \leftarrow (1/2)R_3$):
* New row 3: [0, 0, 1 | -0.5, 0.5, 0.5]
* Augmented matrix becomes:
[1 1 0 |  1    0    0   ]
[0 1 1 |  0    1    0   ]
[0 0 1 | -0.5  0.5  0.5 ]


* **Step 4:** Eliminate the entry above the third pivot in the second row ($R_2 \leftarrow R_2 - R_3$):
* New row 2: [0 - 0, 1 - 0, 1 - 1 | 0 - (-0.5), 1 - 0.5, 0 - 0.5] = [0, 1, 0 | 0.5, 0.5, -0.5]
* Augmented matrix becomes:
[1 1 0 |  1    0    0   ]
[0 1 0 |  0.5  0.5 -0.5 ]
[0 0 1 | -0.5  0.5  0.5 ]


* **Step 5:** Eliminate the entry in the first row above the second pivot ($R_1 \leftarrow R_1 - R_2$):
* New row 1: [1 - 0, 1 - 1, 0 - 0 | 1 - 0.5, 0 - 0.5, 0 - (-0.5)] = [1, 0, 0 | 0.5, -0.5, 0.5]
* Final reduced augmented matrix (with identity on the left):
[1 0 0 |  0.5 -0.5  0.5 ]
[0 1 0 |  0.5  0.5 -0.5 ]
[0 0 1 | -0.5  0.5  0.5 ]




3. **Extracting the Inverse:**
* The right side now holds our inverse matrix $A^{-1}$ (factoring out 0.5 or 1/2 for clarity):
A⁻¹ = 0.5 * [1 -1 1; 1 1 -1; -1 1 1]
*(or in decimal form: [0.5 -0.5 0.5; 0.5 0.5 -0.5; -0.5 0.5 0.5])*


4. **Checking the Result by Multiplication (A * A⁻¹):**
* Multiplying our original matrix $A$ by $A^{-1}$:
[1 1 0; 0 1 1; 1 0 1] * 0.5 * [1 -1 1; 1 1 -1; -1 1 1]
* Evaluating row by row:
* Row 1: [1(1) + 1(1) + 0(-1), 1(-1) + 1(1) + 0(1), 1(1) + 1(-1) + 0(1)] = [2, 0, 0] → scaled by 0.5 gives [1, 0, 0]
* Row 2: [0(1) + 1(1) + 1(-1), 0(-1) + 1(1) + 1(1), 0(1) + 1(-1) + 1(1)] = [0, 2, 0] → scaled by 0.5 gives [0, 1, 0]
* Row 3: [1(1) + 0(1) + 1(-1), 1(-1) + 0(1) + 1(1), 1(1) + 0(-1) + 1(1)] = [0, 0, 2] → scaled by 0.5 gives [0, 0, 1]


* **Conclusion:** The product equals the 3 × 3 identity matrix $I$, verifying that our calculated inverse is correct.
