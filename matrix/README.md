# Matrix

**Table of Contents**

- [Matrix](#matrix)
  - [Spiral Traversal of a Matrix](#spiral-traversal-of-a-matrix)

---

## Spiral Traversal of a Matrix

<details>

  <summary>Information</summary>

1. Clockwise simulation

   - Prepare seen_matrix of size row \* col and fill it when you visited a node for the first them.
   - After hitting the boundary or visiting a node present in seen_matrix, we have to rotate clockwise.
   - Space Complexity is $O(rows * cols)$
   - Time Complexity is $O(rows * cols)$

2. Four loops Iterative

   - run for loops while all the elements in the matrix is printed.
   - create start_row, end_row, start_col, end_col.
   - print the top row, start_row: from start_col to end_col and increment start_row
   - print the right column, end_col: from start_row to end_row and decrement end_col
   - print the bottom row, end_row: from end_col to start_col and decrement end_row
   - print left column, start_col: from end_row to start_row and increment start_col
   - Run the while loop while start_row < end_row and start_col < end_col
   - Space Complexity is $O(1)$
   - Time Complexity is $O(rows * cols)$

3. Four loops Recursive

   - In each recrusive call, we decrease the dimensions of the matrix. The idea of printing the boundary or loops is the same as above.
   - Space Complexity is $O(1)$
   - Time Complexity is $O(rows * cols)$

4. DFS Method

   - create a valid_matrix, and after visiting a node changed the element value at i, j to None
   - check surrounding cells are valid, if not, return result
   - direction right: check right otherwise go down
   - direction down: check down, otherwise go left
   - direction left: check left, otherwise go up
   - direction up: check up, otherwise go right

</details>
