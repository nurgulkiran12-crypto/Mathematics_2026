## Question

Exercise 13. Undoing a Composite Transformation
The matrices:
S = [2 0; 0 1], H = [1 1; 0 1]
describe nonuniform scaling and shear. For T = HS, find T⁻¹ in two ways:

1. first compute T, then its inverse,
2. use (HS)⁻¹ = S⁻¹H⁻¹.
Compare the results. Additionally compute H⁻¹S⁻¹ and verify that the incorrect order gives a different matrix. Explain the rule: “when undoing a composition of operations, we undo them from the end.”

## Solution

1. **Method 1: Compute T First, Then Its Inverse**
* Compute matrix product $T = HS$:
$T = [1 1; 0 1] * [2 0; 0 1] = [(1 \times 2 + 1 \times 0), (1 \times 0 + 1 \times 1); (0 \times 2 + 1 \times 0), (0 \times 0 + 1 \times 1)] = [2 1; 0 1]$
* Compute the determinant of $T$: $\det(T) = (2 \times 1) - (1 \times 0) = 2$.
* Using the 2 × 2 inverse formula:
$T^{-1} = (1 / 2) * [1 -1; 0 2] = [1/2 -1/2; 0 1]$ (or in decimal form: $[0.5\ -0.5;\ 0\ 1]$).


2. **Method 2: Use the Rule $(HS)^{-1} = S^{-1}H^{-1}$**
* Find $S^{-1}$ (reciprocating diagonal entries):
$S^{-1} = [1/2 0; 0 1]$ (or $[0.5\ 0;\ 0\ 1]$)
* Find $H^{-1}$ (using the 2 × 2 formula or by reversing the shear direction):
$H^{-1} = [1 -1; 0 1]$
* Compute the product $S^{-1}H^{-1}$:
$S^{-1}H^{-1} = [1/2 0; 0 1] * [1 -1; 0 1] = [(1/2 \times 1 + 0 \times 0), (1/2 \times -1 + 0 \times 1); (0 \times 1 + 1 \times 0), (0 \times -1 + 1 \times 1)] = [1/2 -1/2; 0 1]$
(or $[0.5\ -0.5;\ 0\ 1]$).


3. **Comparison of Results:**
* Both methods yield the exact same inverse matrix: $[0.5\ -0.5;\ 0\ 1]$.


4. **Computing the Incorrect Order ($H^{-1}S^{-1}$):**
* Compute $H^{-1}S^{-1}$:
$H^{-1}S^{-1} = [1 -1; 0 1] * [1/2 0; 0 1] = [(1 \times 1/2 + -1 \times 0), (1 \times 0 + -1 \times 1); (0 \times 1/2 + 1 \times 0), (0 \times 0 + 1 \times 1)] = [1/2 -1; 0 1]$
(or $[0.5\ -1;\ 0\ 1]$).
* **Verification:** This gives $[0.5\ -1;\ 0\ 1]$, which is clearly different from our correct inverse $[0.5\ -0.5;\ 0\ 1]$, proving that matrix multiplication order matters and the reversed order is mandatory.


5. **Explanation of the Rule (“Undo from the End”):**
* When you apply a composition of transformations like $T = HS$, matrix $S$ acts on the vector first, and matrix $H$ acts on the result second.
* To undo this journey, you must reverse the steps **in reverse order**: you first undo the last thing that happened (applying $H^{-1}$), and then undo the first thing that happened (applying $S^{-1}$).
* Therefore, the inverse of a product reverses the sequence: $(HS)^{-1} = S^{-1}H^{-1}$.
