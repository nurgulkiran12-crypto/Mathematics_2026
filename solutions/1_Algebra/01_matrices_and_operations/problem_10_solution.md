## Question

Exercise 10. Columns of a Matrix Product
Given:
A = [1 2 0; 0 1 1] and B = [1 2; -1 0; 3 1]
Denote the columns of B by b1, b2.

1. Compute Ab1 and Ab2.
2. Compute the matrix AB.
3. Compare the results and explain why the columns of AB are exactly the vectors Ab1 and Ab2.

## Solution

1. **Identifying the Columns of B and Computing Ab1, Ab2:**
* Matrix B (size 3 × 2) has two column vectors:
b1 = [1; -1; 3]
b2 = [2; 0; 1]
* **Computing Ab1:**
Ab1 = [1 2 0; 0 1 1] * [1; -1; 3]
Ab1 = [(1 × 1) + (2 × (-1)) + (0 × 3); (0 × 1) + (1 × (-1)) + (1 × 3)]
Ab1 = [1 - 2 + 0; 0 - 1 + 3] = [-1; 2]
* **Computing Ab2:**
Ab2 = [1 2 0; 0 1 1] * [2; 0; 1]
Ab2 = [(1 × 2) + (2 × 0) + (0 × 1); (0 × 2) + (1 × 0) + (1 × 1)]
Ab2 = [2 + 0 + 0; 0 + 0 + 1] = [2; 1]


2. **Computing the Matrix Product AB:**
* Multiplying matrix A (2 × 3) by matrix B (3 × 2) yields a 2 × 2 matrix:
AB = [1 2 0; 0 1 1] * [1 2; -1 0; 3 1]
AB = [(1 × 1) + (2 × (-1)) + (0 × 3), (1 × 2) + (2 × 0) + (0 × 1); (0 × 1) + (1 × (-1)) + (1 × 3), (0 × 2) + (1 × 0) + (1 × 1)]
AB = [1 - 2 + 0, 2 + 0 + 0; 0 - 1 + 3, 0 + 0 + 1]
AB = [-1 2; 2 1]


3. **Comparison and Explanation:**
* Comparing the columns of our resulting matrix AB with our previous vector products:
* The first column of AB is [-1; 2], which matches **Ab1**.
* The second column of AB is [2; 1], which matches **Ab2**.


* **Explanation:** By definition, matrix multiplication can be viewed column by column. When multiplying matrix A by matrix B, each column of the product AB is formed by multiplying matrix A by the corresponding column of B. Therefore, AB = [Ab1 Ab2], which confirms that the columns of the product matrix are precisely the vectors Ab1 and Ab2.
