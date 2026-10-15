# Matrix Basics: Size, Entries, and Vectors

Let's break this down step-by-step so you can master how to read and navigate matrices easily!

---

## Step 1: Finding the Size of a Matrix (Dimensions)

The **size** (or dimension) of a matrix is always written in the format:
$$\text{Number of Rows} \times \text{Number of Columns}$$
*(A helpful trick to remember the order: **R**ow **C**olumn, like **R**oot **C**eer, or going "down then across".)*

* **Rows** go horizontally (left to right).
* **Columns** go vertically (top to bottom).

### Looking at Matrix $A$:
$$A = \begin{pmatrix} 2 & -1 & 3 \\ 0 & 4 & 5 \end{pmatrix}$$
1. Count the horizontal rows: There is row 1 `(2, -1, 3)` and row 2 `(0, 4, 5)`. That's **2 rows**.
2. Count the vertical columns: Column 1 `(2, 0)`, Column 2 `(-1, 4)`, and Column 3 `(3, 5)`. That's **3 columns**.
* **Result for $A$:** $2 \times 3$

### Looking at Matrix $B$:
$$B = \begin{pmatrix} 1 & 0 \\ -2 & 3 \\ 4 & 1 \end{pmatrix}$$
1. Count the rows (going down): There are **3 rows**.
2. Count the columns (going across): There are **2 columns**.
* **Result for $B$:** $3 \times 2$

---

## Step 2: Reading Specific Entries (Indices)

When you see notation like $a_{12}$ or $b_{21}$, the letters and numbers tell you exactly where to look:
* The **lowercase letter** ($a$ or $b$) refers to the matrix name.
* The **first subscript number** tells you the **Row**.
* The **second subscript number** tells you the **Column**.

So, $a_{12}$ means: *"Look in Matrix $A$, Row 1, Column 2."*

Let's find the ones requested:
* **$a_{12}$ (Row 1, Column 2 of $A$):** Look at the first row of $A$ `(2, -1, 3)` and find the second number in it. That is **$-1$**.
* **$a_{23}$ (Row 2, Column 3 of $A$):** Look at the second row of $A$ `(0, 4, 5)` and find the third number. That is **$5$**.
* **$b_{21}$ (Row 2, Column 1 of $B$):** Look at the second row of $B$ `(-2, 3)` and find the first number. That is **$-2$**.
* **$b_{32}$ (Row 3, Column 2 of $B$):** Look at the third row of $B$ `(4, 1)` and find the second number. That is **$1$**.

---

## Step 3: Writing Rows and Columns as Vectors

A **vector** is just a single line of numbers (either written horizontally as a row vector or vertically as a column vector).

* **The second row of $A$:** We just grab the entire second row of matrix $A$ and write it out:
  $$\begin{pmatrix} 0 & 4 & 5 \end{pmatrix}$$

* **The first column of $B$:** We grab the entire first column of matrix $B$ and write it vertically:
  $$\begin{pmatrix} 1 \\ -2 \\ 4 \end{pmatrix}$$
