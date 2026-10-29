## Question

Exercise 11. When Do Matrices Commute?
Given:
A = [1 1; 0 1] and B = [a b; c d]
Find the conditions on a, b, c, d under which AB = BA. Describe the general form of all such matrices B.

## Solution

1. **Computing AB:**
Multiplying matrix A by matrix B:
AB = [1 1; 0 1] * [a b; c d]
AB = [(1 × a) + (1 × c), (1 × b) + (1 × d); (0 × a) + (1 × c), (0 × b) + (1 × d)]
AB = [a + c, b + d; c, d]
2. **Computing BA:**
Multiplying matrix B by matrix A:
BA = [a b; c d] * [1 1; 0 1]
BA = [(a × 1) + (b × 0), (a × 1) + (b × 1); (c × 1) + (d × 0), (c × 1) + (d × 1)]
BA = [a, a + b; c, c + d]
3. **Setting AB = BA and Finding the Conditions:**
Equating the corresponding entries of AB and BA:
* Top-left: $a + c = a \rightarrow c = 0$
* Top-right: $b + d = a + b \rightarrow d = a$
* Bottom-left: $c = c$ (already satisfied with $c = 0$)
* Bottom-right: $d = c + d \rightarrow c = 0$ (consistent with our first condition)


Thus, the conditions for $AB = BA$ are **c = 0** and **d = a**, with no restrictions on $b$.
4. **General Form of All Such Matrices B:**
Substituting these conditions back into matrix B:
B = [a b; 0 a]
Therefore, any matrix B that commutes with A must be an upper triangular matrix where the diagonal entries are equal ($a = d = a$) and the bottom-left entry is zero ($c = 0$).
