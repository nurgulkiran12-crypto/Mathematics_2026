## Question

Exercise 8. Inverse of a Transformation
The matrix:
S = [2 0; 0 1/2]
describes a scaling of the plane. Find S⁻¹ and explain geometrically what the inverse transformation does. Check the action of the pair S, S⁻¹ on one simple vector.
*(Why this exercise: connects matrix inversion with geometric transformations and visual undoing.)*

## Solution

1. **Finding the Inverse of Matrix S:**
* For a diagonal matrix like $S = [2\ 0;\ 0\ 1/2]$, the inverse is found by simply reciprocating each non-zero entry on the main diagonal.
* Using the 2 × 2 inverse formula to verify:
det(S) = (2 × 1/2) - (0 × 0) = 1 - 0 = 1.
S⁻¹ = (1 / 1) * [1/2 0; 0 2] = [1/2 0; 0 2] (or [0.5 0; 0 2]).


2. **Geometric Explanation of the Inverse Transformation:**
* The original matrix $S$ **stretches the plane horizontally by a factor of 2** and **compresses it vertically by a factor of 1/2**.
* The inverse transformation $S^{-1}$ does the exact opposite: it **compresses the plane horizontally by a factor of 1/2** (halving the x-coordinate) and **stretches the plane vertically by a factor of 2** (doubling the y-coordinate). Geometrically, $S^{-1}$ completely undoes the distortion created by $S$, restoring every point and shape back to its original proportions.


3. **Checking the Action on a Simple Vector:**
* Let us choose the test vector v = [4; 3].
* **Step A (Applying S):**
S * v = [2 0; 0 1/2] * [4; 3] = [(2 * 4) + (0 * 3); (0 * 4) + (1/2 * 3)] = [8; 1.5]
* **Step B (Applying S⁻¹ to the result):**
S⁻¹ * (S * v) = [1/2 0; 0 2] * [8; 1.5] = [(1/2 * 8) + (0 * 1.5); (0 * 8) + (2 * 1.5)] = [4; 3]
* **Conclusion:** Applying $S$ followed by $S^{-1}$ brings the vector right back to its starting coordinates ([4; 3]), verifying that $S^{-1}$ perfectly reverses the transformation.
