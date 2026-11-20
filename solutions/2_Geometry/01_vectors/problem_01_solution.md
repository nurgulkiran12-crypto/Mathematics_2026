## Question

Exercise 1. Vector Operations and Their Meaning
For $u = (2, -1, 3)$ and $v = (-1, 4, 2)$ compute:

$$
u + v, \quad u - v, \quad 3u - 2v
$$

Then verify that $(u + v) - v = u$, and explain geometrically what adding two vectors means.

## Solution

### 1. Computing the Vector Operations

Given $u = (2, -1, 3)$ and $v = (-1, 4, 2)$, we perform each operation component-wise:

**Vector Addition ($u + v$):**

$$
u + v = (2 + (-1), \ -1 + 4, \ 3 + 2) = (1, 3, 5)
$$

**Vector Subtraction ($u - v$):**

$$
u - v = (2 - (-1), \ -1 - 4, \ 3 - 2) = (3, -5, 1)
$$

**Linear Combination ($3u - 2v$):**

First, compute the scalar multiples $3u$ and $2v$:

$$
3u = (3 \cdot 2, \ 3 \cdot (-1), \ 3 \cdot 3) = (6, -3, 9)
$$

$$
2v = (2 \cdot (-1), \ 2 \cdot 4, \ 2 \cdot 2) = (-2, 8, 4)
$$

Now subtract $2v$ from $3u$:

$$
3u - 2v = (6 - (-2), \ -3 - 8, \ 9 - 4) = (8, -11, 5)
$$

### 2. Verifying That $(u + v) - v = u$

Using our result $u + v = (1, 3, 5)$ from above, subtract $v = (-1, 4, 2)$ component-wise:

$$
(u + v) - v = (1 - (-1), \ 3 - 4, \ 5 - 2) = (2, -1, 3)
$$

Since $(2, -1, 3)$ is identical to the original vector $u$, the identity $(u + v) - v = u$ holds.

### 3. Geometric Meaning of Adding Two Vectors

Geometrically, adding two vectors $u$ and $v$ represents **combining two consecutive displacements** in space, which can be visualized in two equivalent ways:

* **Tip-to-Tail (Triangle) Rule:** Place the tail of vector $v$ at the tip (head) of vector $u$. The sum $u + v$ is the single displacement vector starting from the tail of $u$ and ending at the tip of $v$.
* **Parallelogram Rule:** Place both $u$ and $v$ so that their tails start at the same origin point. If you complete the parallelogram formed by $u$ and $v$ as adjacent sides, the sum $u + v$ is the main diagonal starting from that common origin.
