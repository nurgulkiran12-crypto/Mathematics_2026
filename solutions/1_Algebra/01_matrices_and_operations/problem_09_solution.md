## Question

Exercise 9. Composing Transformations
Let:
S = [2 0; 0 1], R = [0 -1; 1 0]
The matrix S describes nonuniform scaling, while R describes a 90° counterclockwise rotation. For:
x = [1; 2]
compute RSx and SRx. Compare the results and explain geometrically why the order of these transformations matters.

## Solution

1. **Computing RSx:**
* First, apply the scaling matrix $S$ to vector $x$:
Sx = [2 0; 0 1] * [1; 2] = [(2 × 1) + (0 × 2); (0 × 1) + (1 × 2)] = [2; 2]
* Next, apply the rotation matrix $R$ to the resulting vector:
RSx = [0 -1; 1 0] * [2; 2] = [(0 × 2) + (-1 × 2); (1 × 2) + (0 × 2)] = [-2; 2]


2. **Computing SRx:**
* First, apply the rotation matrix $R$ to vector $x$:
Rx = [0 -1; 1 0] * [1; 2] = [(0 × 1) + (-1 × 2); (1 × 1) + (0 × 2)] = [-2; 1]
* Next, apply the scaling matrix $S$ to the resulting vector:
SRx = [2 0; 0 1] * [-2; 1] = [(2 × -2) + (0 × 1); (0 × -2) + (1 × 1)] = [-4; 1]


3. **Comparison and Geometric Explanation:**
* Comparing our results:
RSx = [-2; 2]
SRx = [-4; 1]
Therefore, **RSx != SRx**.
* **Geometric Explanation:** Matrix multiplication corresponds to the composition of linear transformations. Computing $RSx$ means stretching the vector along the horizontal axis first and then rotating the modified vector 90° counterclockwise. In contrast, computing $SRx$ means rotating the vector 90° first and then applying the horizontal stretch. Because scaling and rotation do not commute geometrically—stretching a coordinate axis before rotating changes its final spatial orientation compared to stretching it after rotation—the order of operations changes the final outcome.
