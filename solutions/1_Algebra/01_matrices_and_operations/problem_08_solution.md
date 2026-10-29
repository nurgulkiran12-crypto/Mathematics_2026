## Question

Exercise 8. Row Operations and Their Reversibility
For:
A = [1 2 -1; 2 4 1; -1 1 3]
perform, in order:

1. R2 gets R2 - 2R1,
2. R3 gets R3 + R1,
3. interchange R2 and R3.
Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

## Solution

1. **Initial Matrix A:**
A = [1 2 -1; 2 4 1; -1 1 3]
2. **Step 1: Perform R2 gets R2 - 2R1**
* We subtract 2 times the first row from the second row:
* New row 2: [2 - 2(1), 4 - 2(2), 1 - 2(-1)] = [2 - 2, 4 - 4, 1 - (-2)] = [0 0 3]


* Matrix after Step 1:
[1 2 -1; 0 0 3; -1 1 3]


3. **Step 2: Perform R3 gets R3 + R1**
* We add the first row to the third row:
* New row 3: [-1 + 1, 1 + 2, 3 + (-1)] = [0 3 2]


* Matrix after Step 2:
[1 2 -1; 0 0 3; 0 3 2]


4. **Step 3: Interchange R2 and R3**
* We swap row 2 and row 3:
* Matrix after Step 3:
[1 2 -1; 0 3 2; 0 0 3]


5. **Reversing Each Operation:**
* **Reverse of Step 1 ($R_2 \leftarrow R_2 - 2R_1$):** Add 2 times row 1 back to row 2 ($R_2 \leftarrow R_2 + 2R_1$).
* **Reverse of Step 2 ($R_3 \leftarrow R_3 + R_1$):** Subtract row 1 from row 3 ($R_3 \leftarrow R_3 - R_1$).
* **Reverse of Step 3 (Interchange $R_2$ and $R_3$):** Interchange $R_2$ and $R_3$ a second time (swap them back).
