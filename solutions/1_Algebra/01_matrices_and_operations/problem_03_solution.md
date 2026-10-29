## Question

Exercise 3. When Can Matrices Be Multiplied?
The matrix sizes are:
A is 2 × 3, B is 3 × 4, C is 4 × 2, D is 2 × 2.
For the products:
AB, BA, BC, CB, AC, CA, AD, DA
determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

## Solution

**Dimension Compatibility Rule:**
For a product $XY$ to be defined, the number of columns of matrix $X$ must equal the number of rows of matrix $Y$. If $X$ is of size $m \times n$ and $Y$ is of size $n \times p$, the product $XY$ is defined and results in a matrix of size $m \times p$.

Applying this rule to each product:

1. **AB:**
* Sizes: A (2 × 3) and B (3 × 4)
* Compatibility: Columns of A (3) = Rows of B (3) $\rightarrow$ **Defined**
* Result size: **2 × 4**


2. **BA:**
* Sizes: B (3 × 4) and A (2 × 3)
* Compatibility: Columns of B (4) $\neq$ Rows of A (2) $\rightarrow$ **Not defined**


3. **BC:**
* Sizes: B (3 × 4) and C (4 × 2)
* Compatibility: Columns of B (4) = Rows of C (4) $\rightarrow$ **Defined**
* Result size: **3 × 2**


4. **CB:**
* Sizes: C (4 × 2) and B (3 × 4)
* Compatibility: Columns of C (2) $\neq$ Rows of B (3) $\rightarrow$ **Not defined**


5. **AC:**
* Sizes: A (2 × 3) and C (4 × 2)
* Compatibility: Columns of A (3) $\neq$ Rows of C (4) $\rightarrow$ **Not defined**


6. **CA:**
* Sizes: C (4 × 2) and A (2 × 3)
* Compatibility: Columns of C (2) = Rows of A (2) $\rightarrow$ **Defined**
* Result size: **4 × 3**


7. **AD:**
* Sizes: A (2 × 3) and D (2 × 2)
* Compatibility: Columns of A (3) $\neq$ Rows of D (2) $\rightarrow$ **Not defined**


8. **DA:**
* Sizes: D (2 × 2) and A (2 × 3)
* Compatibility: Columns of D (2) = Rows of A (2) $\rightarrow$ **Defined**
* Result size: **2 × 3**
