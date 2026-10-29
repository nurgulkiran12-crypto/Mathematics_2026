## Question

Exercise 4. Matrix Multiplication and Noncommutativity
For:
A = [1 2; 0 1] and B = [2 0; 3 1]
compute AB and BA. Is AB = BA? Use this example to explain what noncommutativity of matrix multiplication means.

## Solution

1. **Computing AB:**
Multiplying matrix A by matrix B row-by-column:
AB = [1 2; 0 1] * [2 0; 3 1]
AB = [(1 × 2) + (2 × 3), (1 × 0) + (2 × 1); (0 × 2) + (1 × 3), (0 × 0) + (1 × 1)]
AB = [2 + 6, 0 + 2; 0 + 3, 0 + 1] = [8 2; 3 1]
2. **Computing BA:**
Multiplying matrix B by matrix A row-by-column:
BA = [2 0; 3 1] * [1 2; 0 1]
BA = [(2 × 1) + (0 × 0), (2 × 2) + (0 × 1); (3 × 1) + (1 × 0), (3 × 2) + (1 × 1)]
BA = [2 + 0, 4 + 0; 3 + 0, 6 + 1] = [2 4; 3 7]
3. **Comparing AB and BA:**
Comparing our results:
AB = [8 2; 3 1]
BA = [2 4; 3 7]
Therefore, **AB != BA**.
4. **Explanation of Noncommutativity:**
Matrix multiplication is **noncommutative**, meaning that the order in which matrices are multiplied changes the outcome. While ordinary numbers follow the commutative property ($ab = ba$), matrices generally do not. Even when both products are valid and well-defined, $AB$ and $BA$ will typically result in entirely different matrices, as demonstrated by this example.
