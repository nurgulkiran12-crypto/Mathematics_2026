# Exercise 7: Identity Matrix, Zero Matrix, and Powers

Given:
$$
A = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}
$$

## 1. $AI$, $IA$, and $A + 0$
* **$AI = A$** and **$IA = A$**: Multiplying by the identity matrix $I$ keeps the matrix unchanged.
* **$A + 0 = A$**: Adding the zero matrix does not change $A$.

## 2. Computing $A^2$ and $A^3$
* **$A^2$:**
  $$
  A^2 = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}
  $$
* **$A^3$:**
  $$
  A^3 = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}
  $$

## 3. Roles and Pattern
* **Roles:** $I$ is the multiplicative identity and $0$ is the additive identity.
* **Pattern:** For any power $n$, 
  $$
  A^n = \begin{pmatrix} 2^n & n \cdot 2^{n-1} \\ 0 & 2^n \end{pmatrix}
  $$
