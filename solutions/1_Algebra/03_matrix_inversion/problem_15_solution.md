## Question

Exercise 15. Two Methods for Solving the Same System
For:
A = [2 1; 1 3], b = [7; 8]
solve Ax = b in two ways:

1. using A⁻¹b,
2. using Gaussian elimination.
Compare both solutions, the number of essential steps, and state which method was simpler in this example.

## Solution

1. **Method 1: Solving Using A⁻¹b**
* First, find the inverse of matrix A = [2 1; 1 3]. The determinant is:
det(A) = (2 × 3) - (1 × 1) = 6 - 1 = 5.
* Using the 2 × 2 inverse formula:
A⁻¹ = (1 / 5) * [3 -1; -1 2] = [3/5 -1/5; -1/5 2/5]
* Next, compute the solution vector x = A⁻¹b by multiplying A⁻¹ by b = [7; 8]:
* x₁ = (3/5 × 7) + (-1/5 × 8) = 21/5 - 8/5 = 13/5 = 2.6
* x₂ = (-1/5 × 7) + (2/5 × 8) = -7/5 + 16/5 = 9/5 = 1.8


* **Result:** x = [13/5; 9/5] (or [2.6; 1.8]).


2. **Method 2: Solving Using Gaussian Elimination**
* Set up the augmented matrix [A | b]:
[2 1 | 7]
[1 3 | 8]
* Swap rows 1 and 2 to place a 1 in the top-left corner for easier arithmetic:
[1 3 | 8]
[2 1 | 7]
* Apply row operation R₂ ← R₂ - 2R₁ to eliminate the entry below the pivot:
* New row 2: [2 - 2(1), 1 - 2(3) | 7 - 2(8)] = [0, -5 | -9]
* Augmented matrix becomes:
[1  3 |  8]
[0 -5 | -9]


* Scale row 2 by -1/5 (R₂ ← (-1/5)R₂):
* Augmented matrix becomes:
[1 3 | 8  ]
[0 1 | 9/5]


* Back-substitute to find x₁ (R₁ ← R₁ - 3R₂):
* x₂ = 9/5
* x₁ = 8 - 3(9/5) = 40/5 - 27/5 = 13/5


* **Result:** x = [13/5; 9/5] (or [2.6; 1.8]).


3. **Comparison and Conclusion:**
* **Consistency:** Both methods yield the exact same solution vector: $x_1 = 13/5$ and $x_2 = 9/5$.
* **Steps and Efficiency:**
* Finding $A^{-1}b$ requires calculating the determinant, forming the inverse matrix (introducing fractions early), and then performing a matrix-vector multiplication.
* Gaussian elimination works directly on the augmented matrix, keeps integers longer until the final division step, and leads straight to the solution.


* **Simpler Method:** For solving a single linear system $Ax = b$, **Gaussian elimination is simpler and more efficient**. Using the matrix inverse is generally reserved for situations where you need to solve $Ax = b$ for many different right-hand side vectors $b$ using a pre-computed $A^{-1}$.
