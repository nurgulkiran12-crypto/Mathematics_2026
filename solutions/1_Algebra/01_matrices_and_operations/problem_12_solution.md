## Question

Exercise 12. Formula for a Matrix Power
Let:
A = [1 1; 0 1]
Compute $A^2$, $A^3$, and $A^4$, and use them to formulate a conjecture for $A^n$. Then assume the formula is true for $n$, multiply by $A$, and explain why you obtain exactly the formula for $n+1$.

## Solution

1. **Computing Successive Powers ($A^2$, $A^3$, $A^4$):**
* **$A^2$:**
$A^2 = A \times A = [1 1; 0 1] \times [1 1; 0 1] = [(1 \times 1) + (1 \times 0), (1 \times 1) + (1 \times 1); (0 \times 1) + (1 \times 0), (0 \times 1) + (1 \times 1)] = [1 2; 0 1]$
* **$A^3$:**
$A^3 = A^2 \times A = [1 2; 0 1] \times [1 1; 0 1] = [(1 \times 1) + (2 \times 0), (1 \times 1) + (2 \times 1); (0 \times 1) + (1 \times 0), (0 \times 1) + (1 \times 1)] = [1 3; 0 1]$
* **$A^4$:**
$A^4 = A^3 \times A = [1 3; 0 1] \times [1 1; 0 1] = [(1 \times 1) + (3 \times 0), (1 \times 1) + (3 \times 1); (0 \times 1) + (1 \times 0), (0 \times 1) + (1 \times 1)] = [1 4; 0 1]$


2. **Formulating a Conjecture for $A^n$:**
Based on the computed powers ($A^1 = [1 1; 0 1]$, $A^2 = [1 2; 0 1]$, $A^3 = [1 3; 0 1]$, $A^4 = [1 4; 0 1]$), we observe that the top-right entry matches the exponent $n$, while the diagonal entries remain 1 and the bottom-left entry remains 0. Therefore, our conjecture is:
$A^n = [1 n; 0 1]$
3. **Proving the Inductive Step ($n$ to $n+1$):**
* Assume the formula holds for a general positive integer $n$:
$A^n = [1 n; 0 1]$
* To find $A^{n+1}$, multiply our expression for $A^n$ by matrix $A$ one more time:
$A^{n+1} = A^n \times A = [1 n; 0 1] \times [1 1; 0 1]$
* Performing the matrix multiplication:
$A^{n+1} = [(1 \times 1) + (n \times 0), (1 \times 1) + (n \times 1); (0 \times 1) + (1 \times 0), (0 \times 1) + (1 \times 1)]$
$A^{n+1} = [1 + 0, 1 + n; 0 + 0, 0 + 1] = [1 (n + 1); 0 1]$
* **Explanation:** By multiplying $A^n$ by $A$, the top-right entry naturally increments from $n$ to $n + 1$ (due to $1 \times 1 + n \times 1$), while the rest of the matrix structure is perfectly preserved. This confirms that if the formula is true for $n$, it is guaranteed to be true for $n + 1$.
