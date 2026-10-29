---

## Question

Exercise 3. Swapping Two Rows
For:
A = [1 2 0; 0 3 1; 2 1 1]
compute det(A). Then form a matrix B by swapping the first and second rows of A.
First predict det(B) using a determinant property, and then verify your prediction by calculation.
*(Why this exercise: demonstrates how elementary row swaps affect the determinant and introduces the sign-reversal rule.)*

## Solution

1. **Computing det(A):**
* Using cofactor expansion along the first column of A = [1 2 0; 0 3 1; 2 1 1]:
det(A) = 1 * det([3 1; 1 1]) - 0 * det([2 0; 1 1]) + 2 * det([2 0; 3 1])
* Evaluating the 2 × 2 determinants:
det(A) = 1 * ((3 * 1) - (1 * 1)) + 2 * ((2 * 1) - (0 * 3))
det(A) = 1 * (3 - 1) + 2 * (2 - 0) = 1(2) + 2(2) = 2 + 4 = 6.


2. **Forming Matrix B by Swapping Rows:**
* Swapping the first row ([1 2 0]) and the second row ([0 3 1]) yields:
B = [0 3 1; 1 2 0; 2 1 1]


3. **Predicting det(B) Using Determinant Properties:**
* **Property:** If two rows of a square matrix are swapped, the determinant of the new matrix is the exact negative of the original matrix's determinant (det(B) = -det(A)).
* **Prediction:** Since det(A) = 6, we predict that **det(B) = -6**.


4. **Verifying the Prediction by Calculation:**
* Computing det(B) using cofactor expansion along the first row of B:
det(B) = 0 * det([2 0; 1 1]) - 3 * det([1 0; 2 1]) + 1 * det([1 2; 2 1])
* Evaluating:
det(B) = 0 - 3 * ((1 * 1) - (0 * 2)) + 1 * ((1 * 1) - (2 * 2))
det(B) = -3 * (1 - 0) + 1 * (1 - 4)
det(B) = -3(1) + 1(-3) = -3 - 3 = -6.
* **Conclusion:** The calculated determinant matches our prediction (det(B) = -6), confirming the row-swap property.
