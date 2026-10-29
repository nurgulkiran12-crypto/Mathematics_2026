## Question

Exercise 6. Parameter and Invertibility
For:
A(t) = [t 1; 2 t]
find all values of t for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

## Solution

1. **Calculating the Determinant of A(t):**
* For a 2 × 2 matrix of the form [a b; c d], the determinant is given by $ad - bc$.
* Applying this formula to our parameterized matrix A(t) = [t 1; 2 t]:
det(A(t)) = (t × t) - (1 × 2) = t² - 2


2. **Finding Values of t for Which the Matrix Is Not Invertible:**
* A square matrix is **not invertible** (singular) if and only if its determinant is equal to zero.
* Setting our determinant equal to zero:
t² - 2 = 0
t² = 2
t = ±√2
* Therefore, the matrix is not invertible when **t = √2** or **t = -√2**.


3. **Relationship to the Determinant Being Zero:**
* The invertibility of a matrix is directly tied to its determinant because the explicit formula for finding the inverse of a 2 × 2 matrix involves dividing every term by its determinant ($\frac{1}{\text{det}(A)}$). If the determinant is zero, this division is undefined.
* Geometrically, a determinant of zero means the linear transformation represented by the matrix collapses the vector space into a lower dimension (flattening 2D space onto a line), which results in a loss of information. Because information is lost, the transformation cannot be undone, making the matrix non-invertible.
