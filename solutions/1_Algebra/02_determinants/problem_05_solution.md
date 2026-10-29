## Question

Exercise 5. Row Operations
For:
A = [1 2 3; 2 1 0; -1 4 2]
find det(A) by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

## Solution

1. **Initial Matrix A:**
A = [1 2 3; 2 1 0; -1 4 2]
2. **Applying Row Operations to Simplify the Matrix:**
* **Step 1 ($R_2 \leftarrow R_2 - 2R_1$):**
* Subtract 2 times the first row from the second row to eliminate the leading entry below the first pivot:
* New row 2: [2 - 2(1), 1 - 2(2), 0 - 2(3)] = [0, -3, -6]


* Matrix becomes:
[1 2 3; 0 -3 -6; -1 4 2]
* *Effect on determinant:* **No change**. Adding a scalar multiple of one row to another row preserves the exact value of the determinant.


* **Step 2 ($R_3 \leftarrow R_3 + R_1$):**
* Add the first row to the third row to eliminate the leading entry in the third row:
* New row 3: [-1 + 1, 4 + 2, 2 + 3] = [0, 6, 5]


* Matrix becomes:
[1 2 3; 0 -3 -6; 0 6 5]
* *Effect on determinant:* **No change**. Row replacement operations do not alter the determinant.


* **Step 3 ($R_3 \leftarrow R_3 + 2R_2$):**
* Add 2 times the second row to the third row to eliminate the entry below the second pivot:
* New row 3: [0 + 2(0), 6 + 2(-3), 5 + 2(-6)] = [0, 0, -7]


* Matrix becomes (in upper triangular form):
[1 2 3; 0 -3 -6; 0 0 -7]
* *Effect on determinant:* **No change**. Row replacement preserves the determinant.




3. **Computing the Determinant:**
* Because every operation we performed was a row replacement (which has a multiplier effect of 1 on the determinant), the determinant of our final upper triangular matrix is identical to the determinant of the original matrix $A$.
* For an upper triangular matrix, the determinant is simply the product of the entries along its main diagonal:
det(A) = 1 × (-3) × (-7) = 21.
