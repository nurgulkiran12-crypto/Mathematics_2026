## Question

Exercise 4. Gauss–Jordan
Find A⁻¹ using the Gauss-Jordan method for:
A = [1 2; 3 5]
Show the augmented matrix [A | I] after successive operations and explain why obtaining I on the left gives the inverse on the right.

## Solution

1. **Setting Up the Augmented Matrix:**
* We start with the augmented matrix [A | I], combining our 2 × 2 matrix with the 2 × 2 identity matrix:
[1 2 | 1 0]
[3 5 | 0 1]


2. **Performing Successive Row Operations:**
* **Step 1:** Eliminate the entry below the first pivot in column 1 by subtracting 3 times the first row from the second row ($R_2 \leftarrow R_2 - 3R_1$):
* New row 2: [3 - 3(1), 5 - 3(2) | 0 - 3(1), 1 - 3(0)] = [0, -1 | -3, 1]
* Augmented matrix becomes:
[1  2 |  1  0]
[0 -1 | -3  1]


* **Step 2:** Scale the second row to make the pivot equal to 1 by multiplying by $-1$ ($R_2 \leftarrow -R_2$):
* New row 2: [0, 1 | 3, -1]
* Augmented matrix becomes:
[1 2 | 1  0]
[0 1 | 3 -1]


* **Step 3:** Eliminate the entry above the second pivot in column 2 by subtracting 2 times the second row from the first row ($R_1 \leftarrow R_1 - 2R_2$):
* New row 1: [1 - 2(0), 2 - 2(1) | 1 - 2(3), 0 - 2(-1)] = [1, 0 | -5, 2]
* Augmented matrix becomes (with the Identity matrix $I$ isolated on the left):
[1 0 | -5  2]
[0 1 |  3 -1]




3. **Extracting the Inverse:**
* Because the left side has successfully been reduced to the identity matrix $I$, the right side now holds the inverse matrix:
A⁻¹ = [-5 2; 3 -1]


4. **Why Obtaining I on the Left Gives A⁻¹ on the Right:**
* Each row operation corresponds to left-multiplying the augmented matrix by an elementary matrix.
* If we let $E$ represent the combined product of all these elementary row operations, applying them to the starting matrix transforms $[A \mid I]$ into $[E A \mid E I]$.
* Since the row operations successfully transform $A$ into the identity matrix, we know that $E A = I$. By the definition of an inverse, this means $E$ must equal $A^{-1}$.
* Consequently, the right side ($E I = E$) automatically becomes $A^{-1}$.
