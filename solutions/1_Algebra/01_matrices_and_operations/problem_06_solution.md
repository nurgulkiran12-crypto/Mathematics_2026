## Question

Exercise 6. Transpose
For:
A = [1 2 3; 4 5 6] and B = [1 0; 2 1; -1 3]
compute $A^T$, $B^T$, and $AB$. Then verify in this example that $(AB)^T = B^T A^T$.

## Solution

1. **Computing Transposes ($A^T$ and $B^T$):**
* Transposing matrix $A$ (swapping its rows and columns to get a 3 × 2 matrix):
$A^T = [1 4; 2 5; 3 6]$
* Transposing matrix $B$ (swapping its rows and columns to get a 2 × 3 matrix):
$B^T = [1 2 -1; 0 1 3]$


2. **Computing the Matrix Product $AB$:**
* Multiplying $A$ (2 × 3) by $B$ (3 × 2) yields a 2 × 2 matrix:
$AB = [1 2 3; 4 5 6] \times [1 0; 2 1; -1 3]$
$AB = [(1 \times 1) + (2 \times 2) + (3 \times (-1)), (1 \times 0) + (2 \times 1) + (3 \times 3); (4 \times 1) + (5 \times 2) + (6 \times (-1)), (4 \times 0) + (5 \times 1) + (6 \times 3)]$
$AB = [1 + 4 - 3, 0 + 2 + 9; 4 + 10 - 6, 0 + 5 + 18]$
$AB = [2 11; 8 23]$


3. **Computing the Transpose of the Product ($(AB)^T$):**
* Transposing the resulting matrix $AB$:
$(AB)^T = [2 8; 11 23]$


4. **Computing $B^T A^T$ and Verification:**
* Multiplying $B^T$ (2 × 3) by $A^T$ (3 × 2):
$B^T A^T = [1 2 -1; 0 1 3] \times [1 4; 2 5; 3 6]$
$B^T A^T = [(1 \times 1) + (2 \times 2) + ((-1) \times 3), (1 \times 4) + (2 \times 5) + ((-1) \times 6); (0 \times 1) + (1 \times 2) + (3 \times 3), (0 \times 4) + (1 \times 5) + (3 \times 6)]$
$B^T A^T = [1 + 4 - 3, 4 + 10 - 6; 0 + 2 + 9, 0 + 5 + 18]$
$B^T A^T = [2 8; 11 23]$
* Comparing the results, $(AB)^T = [2 8; 11 23]$ and $B^T A^T = [2 8; 11 23]$, which confirms that $(AB)^T = B^T A^T$ holds true for this example.
