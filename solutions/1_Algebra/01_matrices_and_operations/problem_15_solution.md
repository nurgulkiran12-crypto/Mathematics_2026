## Question

Exercise 15. Associativity of Multiplication and Different Calculation Paths
Given:
A = [1 2 0; 0 1 1], B = [1 0; 2 1; -1 3], C = [2 1; 0 -1]
Compute (AB)C and A(BC). Compare the results and the number of intermediate operations ((AB)C uses 12 + 8 = 20 scalar multiplications, while A(BC) uses 12 + 12 = 24). Explain what associativity of matrix multiplication means in this example.

## Solution

1. **Computing (AB)C:**
* **Step 1: Compute AB**
Matrix $A$ is $2 \times 3$ and matrix $B$ is $3 \times 2$, so their product $AB$ is a $2 \times 2$ matrix:
$AB = [1 2 0; 0 1 1] \times [1 0; 2 1; -1 3]$
$AB = [(1 \times 1 + 2 \times 2 + 0 \times (-1)), (1 \times 0 + 2 \times 1 + 0 \times 3); (0 \times 1 + 1 \times 2 + 1 \times (-1)), (0 \times 0 + 1 \times 1 + 1 \times 3)]$
$AB = [1 + 4 + 0, 0 + 2 + 0; 0 + 2 - 1, 0 + 1 + 3] = [5 2; 1 4]$
*(Note: This calculation requires $2 \times 2 \times 3 = 12$ scalar multiplications).*
* **Step 2: Compute (AB)C**
Multiplying the $2 \times 2$ matrix $AB$ by the $2 \times 2$ matrix $C$:
$(AB)C = [5 2; 1 4] \times [2 1; 0 -1]$
$(AB)C = [(5 \times 2 + 2 \times 0), (5 \times 1 + 2 \times (-1)); (1 \times 2 + 4 \times 0), (1 \times 1 + 4 \times (-1))]$
$(AB)C = [10 + 0, 5 - 2; 2 + 0, 1 - 4] = [10 3; 2 -3]$
*(Note: This step requires $2 \times 2 \times 2 = 8$ scalar multiplications).*
* **Total scalar multiplications for (AB)C:** $12 + 8 = 20$.




2. **Computing A(BC):**
* **Step 1: Compute BC**
Matrix $B$ is $3 \times 2$ and matrix $C$ is $2 \times 2$, so their product $BC$ is a $3 \times 2$ matrix:
$BC = [1 0; 2 1; -1 3] \times [2 1; 0 -1]$
$BC = [(1 \times 2 + 0 \times 0), (1 \times 1 + 0 \times (-1)); (2 \times 2 + 1 \times 0), (2 \times 1 + 1 \times (-1)); (-1 \times 2 + 3 \times 0), (-1 \times 1 + 3 \times (-1))]$
$BC = [2 + 0, 1 + 0; 4 + 0, 2 - 1; -2 + 0, -1 - 3] = [2 1; 4 1; -2 -4]$
*(Note: This calculation requires $3 \times 2 \times 2 = 12$ scalar multiplications).*
* **Step 2: Compute A(BC)**
Multiplying the $2 \times 3$ matrix $A$ by the $3 \times 2$ matrix $BC$:
$A(BC) = [1 2 0; 0 1 1] \times [2 1; 4 1; -2 -4]$
$A(BC) = [(1 \times 2 + 2 \times 4 + 0 \times (-2)), (1 \times 1 + 2 \times 1 + 0 \times (-4)); (0 \times 2 + 1 \times 4 + 1 \times (-2)), (0 \times 1 + 1 \times 1 + 1 \times (-4))]$
$A(BC) = [2 + 8 + 0, 1 + 2 + 0; 0 + 4 - 2, 0 + 1 - 4] = [10 3; 2 -3]$
*(Note: This step requires $2 \times 2 \times 3 = 12$ scalar multiplications).*
* **Total scalar multiplications for A(BC):** $12 + 12 = 24$.




3. **Comparison of Results and Computational Cost:**
* Both calculation paths yield the exact same resulting matrix: $(AB)C = A(BC) = [10 3; 2 -3]$.
* However, they differ in computational efficiency: grouping as $(AB)C$ requires **20 scalar multiplications**, whereas grouping as $A(BC)$ requires **24 scalar multiplications**.


4. **Explanation of Associativity:**
* **Associativity** means that when multiplying three or more matrices together, the grouping (or order of pairwise multiplications) does not affect the final resulting product.
* While the final matrix is identical regardless of how parentheses are placed, the choice of grouping can significantly change the number of arithmetic operations required. In computer science and applied linear algebra, optimizing the order of matrix multiplications (matrix chain multiplication) is crucial for saving computational resources.
