Exercise 10: Columns of a Matrix Product

Given:
A = [1 2 0; 0 1 1]
B = [1 2; -1 0; 3 1]

Denote the columns of B by b1 and b2:
b1 = [1, -1, 3]^T
b2 = [2, 0, 1]^T

Computing Ab1 and Ab2:
Ab1 = A * b1 = [1(1) + 2(-1) + 0(3); 0(1) + 1(-1) + 1(3)] = [-1, 2]^T
Ab2 = A * b2 = [1(2) + 2(0) + 0(1); 0(2) + 1(0) + 1(1)] = [2, 1]^T

Computing the matrix AB:
AB = A * B = [-1 2; 2 1]

Comparison and Explanation:
The columns of AB are [-1, 2]^T and [2, 1]^T, which are precisely the vectors Ab1 and Ab2. By definition, multiplying matrix A by matrix B results in a matrix whose columns are formed by multiplying A by each individual column of B (AB = [Ab1 Ab2]).
