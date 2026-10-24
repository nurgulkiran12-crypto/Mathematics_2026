Exercise 12. Formula for a Matrix Power

Given:
A = [1 1; 0 1]

Computing A^2, A^3, and A^4:
A^2 = [1 1; 0 1] * [1 1; 0 1] = [1 2; 0 1]
A^3 = A^2 * A = [1 2; 0 1] * [1 1; 0 1] = [1 3; 0 1]
A^4 = A^3 * A = [1 3; 0 1] * [1 1; 0 1] = [1 4; 0 1]

Conjecture for A^n:
Based on the pattern, the general formula is:
A^n = [1 n; 0 1]

Inductive Step (Multiplying by A):
Assume the formula holds for n: A^n = [1 n; 0 1]
To find A^(n+1), multiply A^n by A:
A^(n+1) = [1 n; 0 1] * [1 1; 0 1] = [1  n + 1; 0  1]
This shows that if the formula is true for n, multiplying by A gives the exact formula for n+1.
