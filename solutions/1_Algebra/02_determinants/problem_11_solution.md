## Question

Exercise 11. Shortening the Calculation with Row Operations
Compute:
$\det([1\ 2\ 3;\ 1\ 3\ 4;\ 1\ 4\ 6])$
by first performing row operations that create as many zeros as possible. State which operations do not change the determinant.

## Solution

1. **Initial Matrix A:**
$A = \begin{pmatrix} 1 & 2 & 3 \\ 1 & 3 & 4 \\ 1 & 4 & 6 \end{pmatrix}$
2. **Performing Row Operations to Simplify the Matrix:**
* **Step 1:** Subtract the first row from the second row ($R_2 \leftarrow R_2 - R_1$) and from the third row ($R_3 \leftarrow R_3 - R_1$) to eliminate the leading entries in columns below the pivot:
* New row 2: $[1 - 1,\ 3 - 2,\ 4 - 3] = [0,\ 1,\ 1]$
* New row 3: $[1 - 1,\ 4 - 2,\ 6 - 3] = [0,\ 2,\ 3]$
* Matrix becomes:
$\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 2 & 3 \end{pmatrix}$


* **Step 2:** Subtract 2 times the second row from the third row ($R_3 \leftarrow R_3 - 2R_2$) to create an upper triangular matrix:
* New row 3: $[0 - 2(0),\ 2 - 2(1),\ 3 - 2(1)] = [0,\ 0,\ 1]$
* Matrix becomes (in upper triangular form):
$\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 0 & 1 \end{pmatrix}$




3. **Computing the Determinant:**
* For an upper triangular matrix, the determinant is simply the product of the entries along its main diagonal:
$\det(A) = 1 \times 1 \times 1 = 1$.


4. **Row Operations That Do Not Change the Determinant:**
* **Adding a scalar multiple of one row to another row** ($R_i \leftarrow R_i + cR_j$) **does not change the determinant** at all. This is the exact property we used above (replacing $R_2$ with $R_2 - R_1$ and $R_3$ with $R_3 - 2R_2$).
* *(Note for context: Multiplying a row by a scalar $c$ scales the determinant by $c$, and swapping two rows multiplies the determinant by $-1$, but row replacement operations preserve the exact value of the determinant).*
