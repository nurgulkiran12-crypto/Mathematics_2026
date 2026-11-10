## Question

Exercise 11. A Parameter in a System of Three Equations
Analyze the number of solutions depending on $t$:


$$\begin{cases} x + y + z = 1 \\ x + ty + z = 2 \\ x + y + tz = 3 \end{cases}$$


Use elimination and separately analyze the parameter values for which a standard calculation step ceases to be valid.
*(Why this exercise: demonstrates how parameters affect pivot positions in larger $3 \times 3$ systems, pinpointing exact breakdown points where unique solutions give way to inconsistency.)*

## Solution

1. **Setting Up the Augmented Matrix:**
* We write the linear system as an augmented matrix $[A \mid b]$:

$$\begin{pmatrix} 1 & 1 & 1 & \big\vert{} & 1 \\ 1 & t & 1 & \big\vert{} & 2 \\ 1 & 1 & t & \big\vert{} & 3 \end{pmatrix}$$




2. **Applying Gaussian Elimination:**
* **Step 1:** Eliminate the leading entry in row 2 by subtracting row 1 from row 2 ($R_2 \leftarrow R_2 - R_1$):
* New row 2: $[1 - 1, \ t - 1, \ 1 - 1 \mid 2 - 1] = [0, \ t - 1, \ 0 \mid 1]$


* **Step 2:** Eliminate the leading entry in row 3 by subtracting row 1 from row 3 ($R_3 \leftarrow R_3 - R_1$):
* New row 3: $[1 - 1, \ 1 - 1, \ t - 1 \mid 3 - 1] = [0, \ 0, \ t - 1 \mid 2]$


* The augmented matrix simplifies directly to upper-triangular form:

$$\begin{pmatrix} 1 & 1 & 1 & \big\vert{} & 1 \\ 0 & t - 1 & 0 & \big\vert{} & 1 \\ 0 & 0 & t - 1 & \big\vert{} & 2 \end{pmatrix}$$




3. **Analyzing Where Standard Calculation Steps Cease to Be Valid:**
* The pivot elements along the diagonal are $1$, $(t - 1)$, and $(t - 1)$.
* A standard elimination or back-substitution step (such as dividing by a pivot to isolate variables) **ceases to be valid when $t - 1 = 0 \implies t = 1$**.
* At $t = 1$, the matrix pivots vanish, preventing normal division and requiring a separate case analysis.


4. **Case-by-Case Analysis Based on $t$:**
* **Case 1: $t = 1$ (Critical Value)**
* Substituting $t = 1$ into our upper-triangular matrix gives:

$$\begin{pmatrix} 1 & 1 & 1 & \big\vert{} & 1 \\ 0 & 0 & 0 & \big\vert{} & 1 \\ 0 & 0 & 0 & \big\vert{} & 2 \end{pmatrix}$$


* Translating Row 2 back into equation form gives $0x + 0y + 0z = 1 \implies 0 = 1$, which is an impossible contradiction.
* **Result:** For **$t = 1$**, the system has **no solution** (inconsistent).


* **Case 2: $t \neq 1$ (General Case)**
* Since $t \neq 1$, we have $t - 1 \neq 0$, allowing us to safely perform back-substitution:
* From Row 3: $(t - 1)z = 2 \implies$ **$z = \frac{2}{t - 1}$**
* From Row 2: $(t - 1)y = 1 \implies$ **$y = \frac{1}{t - 1}$**
* From Row 1 ($x + y + z = 1$):

$$x + \frac{1}{t - 1} + \frac{2}{t - 1} = 1 \implies x + \frac{3}{t - 1} = 1$$


$$x = 1 - \frac{3}{t - 1} = \frac{(t - 1) - 3}{t - 1} \implies$$



**$x = \frac{t - 4}{t - 1}$**


* **Result:** For **all $t \neq 1$**, the system has **exactly one unique solution**:

$$(x, y, z) = \left( \frac{t - 4}{t - 1}, \frac{1}{t - 1}, \frac{2}{t - 1} \right)$$
