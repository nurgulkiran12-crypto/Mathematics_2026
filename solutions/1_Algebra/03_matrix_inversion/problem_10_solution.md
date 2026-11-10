## Question

Exercise 10. Inverse of a Diagonal Matrix
Given:
D = [2 0 0; 0 -3 0; 0 0 5], E = [2 0 0; 0 0 0; 0 0 5]
Without using Gauss-Jordan elimination, decide which matrix is invertible. For the invertible matrix, give the inverse and check the result by multiplication.

## Solution

1. **Determining Invertibility:**
* For a square diagonal matrix, the determinant is simply the product of the entries along its main diagonal.
* For matrix D: det(D) = 2 × (-3) × 5 = -30. Since the determinant is non-zero (det(D) ≠ 0), **matrix D is invertible**.
* For matrix E: det(E) = 2 × 0 × 5 = 0. Since the determinant is zero, **matrix E is not invertible** (singular, because it contains a zero on its diagonal).


2. **Finding the Inverse of Matrix D:**
* The inverse of any diagonal matrix is found by simply reciprocating each non-zero entry on its main diagonal.
* Reciprocating 2, -3, and 5 gives:
D⁻¹ = [1/2 0 0; 0 -1/3 0; 0 0 1/5] (or in decimal form: [0.5 0 0; 0 -0.333 0; 0 0 0.2]).


3. **Checking the Result by Multiplication (D * D⁻¹):**
* Multiply matrix D by our calculated inverse D⁻¹:
D * D⁻¹ = [2 0 0; 0 -3 0; 0 0 5] * [1/2 0 0; 0 -1/3 0; 0 0 1/5]
* Multiplying corresponding diagonal elements:
* Row 1: (2 × 1/2) = 1
* Row 2: (-3 × -1/3) = 1
* Row 3: (5 × 1/5) = 1


* The product yields:
[1 0 0; 0 1 0; 0 0 1]
* **Conclusion:** Because the product equals the 3 × 3 identity matrix, our calculated inverse for matrix D is verified as correct.
