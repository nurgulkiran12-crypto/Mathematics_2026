# Exercise 3: Matrix Multiplication Compatibility

Let's learn how to check if matrices can be multiplied and find the size of the result!

---

## The Golden Rule for Matrix Multiplication

For a product $XY$ to be defined, the **inner dimensions** must match:
* If $X$ is of size $m \times n$ and $Y$ is of size $p \times q$, then $XY$ is defined **if and only if $n = p$**.
* If they match, the resulting matrix has the **outer dimensions**: $m \times q$.

*Quick formula to remember:* 
$$(m \times \mathbf{n}) \times (\mathbf{n} \times q) \implies \text{Valid! Result is } m \times q$$

Given sizes:
* $A$ is $2 \times 3$
* $B$ is $3 \times 4$
* $C$ is $4 \times 2$
* $D$ is $2 \times 2$

---

## Evaluating Each Product

### 1. $AB$ ($A_{2 \times 3} B_{3 \times 4}$)
* **Inner dimensions:** $3$ and $3$ (**Match!**)
* **Status:** **Defined**
* **Result Size:** $2 \times 4$

### 2. $BA$ ($B_{3 \times 4} A_{2 \times 3}$)
* **Inner dimensions:** $4$ and $2$ (Do not match)
* **Status:** **Not defined**

### 3. $BC$ ($B_{3 \times 4} C_{4 \times 2}$)
* **Inner dimensions:** $4$ and $4$ (**Match!**)
* **Status:** **Defined**
* **Result Size:** $3 \times 2$

### 4. $CB$ ($C_{4 \times 2} B_{3 \times 4}$)
* **Inner dimensions:** $2$ and $3$ (Do not match)
* **Status:** **Not defined**

### 5. $AC$ ($A_{2 \times 3} C_{4 \times 2}$)
* **Inner dimensions:** $3$ and $4$ (Do not match)
* **Status:** **Not defined**

### 6. $CA$ ($C_{4 \times 2} A_{2 \times 3}$)
* **Inner dimensions:** $2$ and $2$ (**Match!**)
* **Status:** **Defined**
* **Result Size:** $4 \times 3$

### 7. $AD$ ($A_{2 \times 3} D_{2 \times 2}$)
* **Inner dimensions:** $3$ and $2$ (Do not match)
* **Status:** **Not defined**

### 8. $DA$ ($D_{2 \times 2} A_{2 \times 3}$)
* **Inner dimensions:** $2$ and $2$ (**Match!**)
* **Status:** **Defined**
* **Result Size:** $2 \times 3$
