## Question

Exercise 14. A Small Change in the Right-Hand Side
Compare the systems:


$$\begin{cases} x + y = 2 \\ 2x - y = 1 \\ 3x = 3 \end{cases}$$


and


$$\begin{cases} x + y = 2 \\ 2x - y = 1 \\ 3x = 3.1 \end{cases}$$


Check the consistency of each system and explain why a small change in one number can change the type of the system.
*(Why this exercise: illustrates how overdetermined systems with more equations than unknowns behave, and how sensitive they are to slight changes in the right-hand side vector.)*

## Solution

1. **Analyzing System 1:**
* Let's solve the first two equations simultaneously:
* Adding Eq. 1 and Eq. 2: $(x + y) + (2x - y) = 2 + 1 \implies 3x = 3 \implies$ **$x = 1$**.
* Substitute $x = 1$ into Eq. 1: $1 + y = 2 \implies$ **$y = 1$**.


* Now, check if this solution satisfies the third equation ($3x = 3$):
* $3(1) = 3$, which is completely true.


* **Conclusion for System 1:** The system has a unique solution $(x, y) = (1, 1)$ and is **consistent**. All three lines intersect at the exact same point in the 2D plane.


2. **Analyzing System 2:**
* The first two equations remain identical, uniquely fixing the intersection point at **$x = 1, y = 1$**.
* Now, check the third equation ($3x = 3.1$) using $x = 1$:
* $3(1) = 3.1 \implies 3 = 3.1$, which is a mathematical contradiction ($0 = 0.1$).


* **Conclusion for System 2:** Because no point can satisfy all three equations simultaneously, the system has **no solution** and is **inconsistent**.


3. **Explaining Why a Small Change Changes the System Type:**
* **Geometric Perspective:** Each equation represents a straight line in the 2D plane. A system with two variables and three equations is *overdetermined* (more constraints than dimensions).
* In **System 1**, the third line happens to pass directly through the intersection point of the first two lines, meaning all three lines share a common meeting point.
* In **System 2**, changing the right-hand side from $3$ to $3.1$ shifts the third line slightly parallel to itself. While the first two lines still intersect at $(1, 1)$, the third line now requires $x = \frac{3.1}{3} \approx 1.033$. The three lines now form a triangle with three separate intersection vertices rather than a single common point.
* This demonstrates that overdetermined systems are often **unstable to perturbations** in the right-hand side vector $b$ unless the perturbation lies precisely within the column space of the coefficient matrix.
