## Question

Exercise 9. Area and the Determinant
The vectors:
u = [3; 1], v = [1; 4]
span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.
*(Why this exercise: gives the determinant a geometric interpretation and distinguishes its sign from the value of the area.)*

## Solution

1. **Computing the Determinant and Area in the Original Order:**
* Form a 2 × 2 matrix $M$ using vectors $u$ and $v$ as its columns:
$M = [u \ v] = [3 1; 1 4]$
* Compute the determinant of $M$:
$\det(M) = (3 \times 4) - (1 \times 1) = 12 - 1 = 11$
* The area of the parallelogram spanned by two vectors is given by the absolute value of their determinant:
$\text{Area} = \vert{}\det(M)\vert{} = \vert{}11\vert{} = 11$


2. **Reversing the Order of the Vectors:**
* Form the new matrix $M'$ by placing $v$ first and $u$ second:
$M' = [v \ u] = [1 3; 4 1]$
* Compute the new determinant:
$\det(M') = (1 \times 1) - (3 \times 4) = 1 - 12 = -11$


3. **Explanation (Determinant Sign vs. Area):**
* **What changes in the determinant:** The sign of the determinant flips from $+11$ to $-11$. Swapping the columns of a matrix changes the sign of its determinant because it alters the orientation (or handedness) of the coordinate system defined by the vectors.
* **What does not change in the area:** The numerical value of the area remains exactly the same ($11$). Geometric area represents a magnitude, which must always be non-negative. Taking the absolute value of the determinant strips away the sign, ensuring the area is invariant to the order in which the vectors are listed.
