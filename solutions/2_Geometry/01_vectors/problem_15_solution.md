## Question

Exercise 15. Comparing Directions Using the Cosine of the Angle
Given:

$$a = (1, 2, 1), \quad b = (2, 4, 2), \quad c = (2, 0, 3)$$

For each pair, compute:

$$\frac{u \cdot v}{\Vert{}u\Vert{}\Vert{}v\Vert{}}$$

Order the pairs by increasing angle between the vectors. Explain why for $a$ and $b$ the value is $1$ even though the vectors have different lengths.

## Solution

### 1. Computing the Euclidean Norms (Magnitudes) of $a$, $b$, and $c$

**Mechanism Used:** 3D Euclidean norm ($L_2$-norm) formula $\Vert{}u\Vert{} = \sqrt{u_1^2 + u_2^2 + u_3^2}$ to determine the length of each vector before normalizing their dot products.

* **Magnitude of $a = (1, 2, 1)$:**

$$\Vert{}a\Vert{} = \sqrt{1^2 + 2^2 + 1^2} = \sqrt{1 + 4 + 1} = \sqrt{6}$$

* **Magnitude of $b = (2, 4, 2)$:**

$$\Vert{}b\Vert{} = \sqrt{2^2 + 4^2 + 2^2} = \sqrt{4 + 16 + 4} = \sqrt{24} = 2\sqrt{6}$$

* **Magnitude of $c = (2, 0, 3)$:**

$$\Vert{}c\Vert{} = \sqrt{2^2 + 0^2 + 3^2} = \sqrt{4 + 0 + 9} = \sqrt{13}$$

### 2. Computing $\cos\theta = \frac{u \cdot v}{\Vert{}u\Vert{}\Vert{}v\Vert{}}$ for Each Vector Pair

**Mechanism Used:** Normalized dot product (cosine similarity), which divides the Euclidean dot product $u \cdot v = u_1 v_1 + u_2 v_2 + u_3 v_3$ by the product of the vector lengths $\Vert{}u\Vert{}\Vert{}v\Vert{}$.

#### Pair 1: $(a, b)$

* **Dot product:**

$$a \cdot b = (1)(2) + (2)(4) + (1)(2) = 2 + 8 + 2 = 12$$

* **Cosine of angle $\theta_{ab}$:**

$$\cos\theta_{ab} = \frac{a \cdot b}{\Vert{}a\Vert{}\Vert{}b\Vert{}} = \frac{12}{\sqrt{6} \cdot 2\sqrt{6}} = \frac{12}{2 \cdot 6} = \frac{12}{12} = 1$$

#### Pair 2: $(a, c)$

* **Dot product:**

$$a \cdot c = (1)(2) + (2)(0) + (1)(3) = 2 + 0 + 3 = 5$$

* **Cosine of angle $\theta_{ac}$:**

$$\cos\theta_{ac} = \frac{a \cdot c}{\Vert{}a\Vert{}\Vert{}c\Vert{}} = \frac{5}{\sqrt{6}\sqrt{13}} = \frac{5}{\sqrt{78}} \approx 0.5661$$

#### Pair 3: $(b, c)$

* **Dot product:**

$$b \cdot c = (2)(2) + (4)(0) + (2)(3) = 4 + 0 + 6 = 10$$

* **Cosine of angle $\theta_{bc}$:**

$$\cos\theta_{bc} = \frac{b \cdot c}{\Vert{}b\Vert{}\Vert{}c\Vert{}} = \frac{10}{2\sqrt{6}\sqrt{13}} = \frac{10}{2\sqrt{78}} = \frac{5}{\sqrt{78}} \approx 0.5661$$

### 3. Ordering the Pairs by Increasing Angle (with Verification Check)

**Mechanism Used:** Monotonicity of $\cos\theta$ on $[0^\circ, 180^\circ]$—on this interval, $\cos\theta$ is strictly decreasing, so a **larger cosine** corresponds to a **smaller angle** $\theta$.

Comparing our computed cosines:

$$\cos\theta_{ab} = 1 > \cos\theta_{ac} = \cos\theta_{bc} = \frac{5}{\sqrt{78}} \approx 0.5661$$

**Verification Check (Exact Angle Values via $\arccos$):**

* **For $(a, b)$:** $\theta_{ab} = \arccos(1) = 0^\circ$ ($0\text{ rad}$).
* **For $(a, c)$ and $(b, c)$:** $\theta_{ac} = \theta_{bc} = \arccos\left(\frac{5}{\sqrt{78}}\right) \approx 55.52^\circ$ ($0.969\text{ rad}$).

**Order by Increasing Angle:**

$$
\theta_{ab} = 0^\circ < \theta_{ac} = \theta_{bc} \approx 5

<img width="2816" height="1536" alt="image" src="https://github.com/user-attachments/assets/df33d1c7-4f44-4444-87d9-1ec75f9b5156" />
