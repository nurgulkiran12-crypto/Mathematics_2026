## Question

Exercise 7. Identity and Zero Matrices, and Powers of a Matrix
For:
A = [2 1; 0 2]
compute:
AI, IA, A + 0, A², A³.
Explain the roles of the matrices I and 0, and describe the pattern you observe in successive powers of A.

## Solution

1. **Computing Neutral-Element Operations:**
* **AI:**
$AI = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (2 \times 1) + (1 \times 0) & (2 \times 0) + (1 \times 1) \\ (0 \times 1) + (2 \times 0) & (0 \times 0) + (2 \times 1) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$
* **IA:**
$IA = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} (1 \times 2) + (0 \times 0) & (1 \times 1) + (0 \times 2) \\ (0 \times 2) + (1 \times 0) & (0 \times 1) + (1 \times 2) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$
* **A + 0:**
$A + 0 = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} + \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix} = \begin{pmatrix} 2 + 0 & 1 + 0 \\ 0 + 0 & 2 + 0 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$


2. **Computing Powers of Matrix A ($A^2$ and $A^3$):**
* **$A^2$:**
$A^2 = A \times A = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} (2 \times 2) + (1 \times 0) & (2 \times 1) + (1 \times 2) \\ (0 \times 2) + (2 \times 0) & (0 \times 1) + (2 \times 2) \end{pmatrix} = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}$
* **$A^3$:**
$A^3 = A^2 \times A = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} (4 \times 2) + (4 \times 0) & (4 \times 1) + (4 \times 2) \\ (0 \times 2) + (4 \times 0) & (0 \times 1) + (4 \times 2) \end{pmatrix} = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}$


3. **Explanation of the Roles of I and 0:**
* **The Identity Matrix ($I$):** Acts as the multiplicative neutral element. Multiplying any square matrix by the identity matrix leaves it completely unchanged ($AI = IA = A$).
* **The Zero Matrix ($0$):** Acts as the additive neutral element. Adding the zero matrix to any matrix leaves it unchanged ($A + 0 = A$).


4. **Description of the Pattern in Successive Powers of A:**
Observing the progression of powers:
$A^1 = \begin{pmatrix} 2^1 & 1 \times 2^0 \\ 0 & 2^1 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$
$A^2 = \begin{pmatrix} 2^2 & 2 \times 2^1 \\ 0 & 2^2 \end{pmatrix} = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}$
$A^3 = \begin{pmatrix} 2^3 & 3 \times 2^2 \\ 0 & 2^3 \end{pmatrix} = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}$
**Pattern:** For any positive integer $n$, the diagonal entries grow as $2^n$, while the top-right entry follows the formula $n \times 2^{n-1}$, and the bottom-left entry remains permanently zero.
