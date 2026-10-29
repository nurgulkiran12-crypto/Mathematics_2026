Question
Exercise 2. Addition and Scalar Multiplication
For:
A = [1 2; -1 3] and B = [4 -2; 0 5]
compute:
A + B, A - B, 3A - 2B.
Explain why matrix addition is possible only for matrices of the same size.

Solution
Computing A + B:
A + B = [1 + 4, 2 + (-2); -1 + 0, 3 + 5] = [5 0; -1 8]

Computing A - B:
A - B = [1 - 4, 2 - (-2); -1 - 0, 3 - 5] = [-3 4; -1 -2]

Computing 3A - 2B:

First, scalar multiplication:
3A = [3 × 1, 3 × 2; 3 × (-1), 3 × 3] = [3 6; -3 9]
2B = [2 × 4, 2 × (-2); 2 × 0, 2 × 5] = [8 -4; 0 10]

Then, subtract the resulting matrices:
3A - 2B = [3 - 8, 6 - (-4); -3 - 0, 9 - 10] = [-5 10; -3 -1]

Explanation of the Size Requirement:
Matrix addition and subtraction are performed element-by-element (entrywise). Therefore, both matrices must have the exact same dimensions (same number of rows and columns) so that every element in matrix A has a corresponding matching element in matrix B to add or subtract with. If their sizes differed, some entries would not have a partner.
