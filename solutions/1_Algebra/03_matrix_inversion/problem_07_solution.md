## Question

Exercise 7. Inverse of a Product
For:
A = [1 1; 0 1], B = [2 0; 0 3]
compute (AB)⁻¹ and B⁻¹A⁻¹. Check that the results are the same and explain the meaning of the reversed order.

## Solution

1. **Computing (AB)⁻¹:**
* First, find the matrix product AB:
AB = [1 1; 0 1] * [2 0; 0 3]
AB = [(1 * 2) + (1 * 0), (1 * 0) + (1 * 3); (0 * 2) + (1 * 0), (0 * 0) + (1 * 3)]
AB = [2 3; 0 3]
* Next, compute the inverse of AB. The determinant is det(AB) = (2 × 3) - (3 × 0) = 6.
* Using the 2 × 2 inverse formula:
(AB)⁻¹ = (1 / 6) * [3 -3; 0 2] = [3/6 -3/6; 0 2/6] = [1/2 -1/2; 0 1/3] (or [0.5 -0.5; 0 0.333]).


2. **Computing Individual Inverses (A⁻¹ and B⁻¹):**
* For A = [1 1; 0 1]:
det(A) = (1 × 1) - (1 × 0) = 1.
A⁻¹ = [1 -1; 0 1].
* For B = [2 0; 0 3]:
det(B) = (2 × 3) - (0 × 0) = 6.
B⁻¹ = (1 / 6) * [3 0; 0 2] = [3/6 0; 0 2/6] = [1/2 0; 0 1/3].


3. **Computing the Product B⁻¹A⁻¹:**
* Multiply B⁻¹ by A⁻¹:
B⁻¹A⁻¹ = [1/2 0; 0 1/3] * [1 -1; 0 1]
B⁻¹A⁻¹ = [(1/2 * 1) + (0 * 0), (1/2 * -1) + (0 * 1); (0 * 1) + (1/3 * 0), (0 * -1) + (1/3 * 1)]
B⁻¹A⁻¹ = [1/2 -1/2; 0 1/3]
* **Check:** Both $(AB)^{-1}$ and $B^{-1}A^{-1}$ yield the exact same matrix: `[1/2 -1/2; 0 1/3]`.


4. **Explaining the Meaning of the Reversed Order:**
* **Logical sequence:** If you perform matrix transformation A followed by matrix transformation B, the combined operation is represented by the product $AB$.
* **Undoing the process:** To reverse or undo this combined transformation, you must reverse the steps in **reverse order**: you must first undo the last applied operation ($B$), which requires applying $B^{-1}$, and then undo the first operation ($A$), which requires applying $A^{-1}$.
* Therefore, the inverse of a product is always the product of the inverses in reverse: $(AB)^{-1} = B^{-1}A^{-1}$.
