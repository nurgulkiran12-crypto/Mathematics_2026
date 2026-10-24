# Exercise 3: When Can Matrices Be Multiplied?

Given matrix sizes: $A_{2\times3}$, $B_{3\times4}$, $C_{4\times2}$, $D_{2\times2}$.

## Analysis of Products

* **$AB$ ($2\times3$ and $3\times4$):** Inner dimensions match ($3 = 3$). **Defined**, result size is **$2 \times 4$**.
* **$BA$ ($3\times4$ and $2\times3$):** Inner dimensions do not match ($4 \neq 2$). **Undefined**.
* **$BC$ ($3\times4$ and $4\times2$):** Inner dimensions match ($4 = 4$). **Defined**, result size is **$3 \times 2$**.
* **$CB$ ($4\times2$ and $3\times4$):** Inner dimensions do not match ($2 \neq 3$). **Undefined**.
* **$AC$ ($2\times3$ and $4\times2$):** Inner dimensions do not match ($3 \neq 4$). **Undefined**.
* **$CA$ ($4\times2$ and $2\times3$):** Inner dimensions match ($2 = 2$). **Defined**, result size is **$4 \times 3$**.
* **$AD$ ($2\times3$ and $2\times2$):** Inner dimensions do not match ($3 \neq 2$). **Undefined**.
* **$DA$ ($2\times2$ and $2\times3$):** Inner dimensions match ($2 = 2$). **Defined**, result size is **$2 \times 3$**.
