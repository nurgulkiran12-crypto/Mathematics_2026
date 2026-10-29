## Question

Exercise 13. A Recurrence Written in Matrix Form
Let:
F = [1 1; 1 0]
Compute F², F³, F⁴, and F⁵. Compare the numbers obtained with the sequence 0, 1, 1, 2, 3, 5, 8, … and describe the relationship you observe. Then compute:
F * [a; b]
and explain how this multiplication performs one recurrence step: it creates the sum of two consecutive terms and keeps one of them for the next step.

## Solution

1. **Computing Successive Powers of F ($F^2, F^3, F^4, F^5$):**
* **$F$ (Base matrix):**
$F = [1 1; 1 0]$
* **$F^2$:**
$F^2 = F \times F = [1 1; 1 0] \times [1 1; 1 0] = [(1 \times 1 + 1 \times 1), (1 \times 1 + 1 \times 0); (1 \times 1 + 0 \times 1), (1 \times 1 + 0 \times 0)] = [2 1; 1 1]$
* **$F^3$:**
$F^3 = F^2 \times F = [2 1; 1 1] \times [1 1; 1 0] = [(2 \times 1 + 1 \times 1), (2 \times 1 + 1 \times 0); (1 \times 1 + 1 \times 1), (1 \times 1 + 1 \times 0)] = [3 2; 2 1]$
* **$F^4$:**
$F^4 = F^3 \times F = [3 2; 2 1] \times [1 1; 1 0] = [(3 \times 1 + 2 \times 1), (3 \times 1 + 2 \times 0); (2 \times 1 + 1 \times 1), (2 \times 1 + 1 \times 0)] = [5 3; 3 2]$
* **$F^5$:**
$F^5 = F^4 \times F = [5 3; 3 2] \times [1 1; 1 0] = [(5 \times 1 + 3 \times 1), (5 \times 1 + 3 \times 0); (3 \times 1 + 2 \times 1), (3 \times 1 + 2 \times 0)] = [8 5; 5 3]$


2. **Comparison with the Fibonacci Sequence:**
* The given sequence $0, 1, 1, 2, 3, 5, 8, \dots$ is the famous **Fibonacci sequence**, where each term is the sum of the two preceding ones.
* **Relationship:** The entries of the matrices $F^n$ are composed entirely of consecutive Fibonacci numbers. For instance, the entries of $F^5$ are 8, 5, and 3, which appear directly in the sequence. In general, the matrix power $F^n$ contains Fibonacci numbers such that $F^n = [F_{n+1} F_n; F_n F_{n-1}]$.


3. **Computing $F \times [a; b]$:**
* Multiplying matrix $F$ by vector $[a; b]$:
$F \times [a; b] = [1 1; 1 0] \times [a; b] = [(1 \times a + 1 \times b); (1 \times a + 0 \times b)] = [a + b; a]$


4. **Explanation of the Recurrence Step:**
* When we apply matrix $F$ to a vector containing two consecutive terms $[a; b]$ (where $a$ is the current term and $b$ is the previous term), the resulting vector is $[a + b; a]$.
* **How it works:**
* The top entry ($a + b$) calculates the sum of the two terms, generating the **next** term in the recurrence sequence.
* The bottom entry ($a$) retains the current term, shifting it down to serve as the previous term for the subsequent step.
* This elegant matrix multiplication acts as a machine that steps a recurrence relation forward by one generation.
