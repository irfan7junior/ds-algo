# Matrix

**Table of Contents**

- [Matrix](#matrix)
  - [Spiral Traversal of a Matrix](#spiral-traversal-of-a-matrix)
  - [Search in sorted matrix](#search-in-sorted-matrix)
  - [Finding median in a row sorted matrix](#finding-median-in-a-row-sorted-matrix)
  - [Row with max number of 1s](#row-with-max-number-of-1s)
  - [Print elements in sorted order using row-colum wise sorted matrix](#print-elements-in-sorted-order-using-row-colum-wise-sorted-matrix)
  - [Max Area under Histogram](#max-area-under-histogram)
  - [Max Area Rectangle](#max-area-rectangle)
  - [Find a specific pair in matrix](#find-a-specific-pair-in-matrix)
  - [Rotate the matrix by 90deg](#rotate-the-matrix-by-90deg)

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

## Search in sorted matrix

<details>

  <summary>Implementation</summary>

- i = 0, j = cols - 1
- while i >= 0 and j >= 0 and i < rows and j < cols, do
- matrix[i][j] == target, return i, j
- else if matrix[i][j] < target, i += 1
- else if matrix[i][j] > target, j -= 1
- return None
- Time Complexity is, $O(n + m)$
- Space Complexity is, $O(1)$

</details>

## Finding median in a row sorted matrix

<details>

  <summary>Implementation</summary>

1. Sorting method

   - convert the matrix into an array of integers
   - sort them
   - find the rank of median by (len(array) + 1) / 2 = rank
   - return array[rank - 1]
   - Time Complexity is, $O(rows*cols*log(rows*cols))$
   - Space Complexity is, $O(rows*cols)$

</details>

## Row with max number of 1s

<details>

  <summary>Implementation</summary>

- create max_1s_row = -1
- iterate through each row
- do a binary search to find the first value equal to 1, subtract it cols
- update max_1s_row
- return its value finally
- Time Complexity is, $O(rows * log(cols))$
- Space Complexity is, $O(1)$

</details>

## Print elements in sorted order using row-colum wise sorted matrix

<details>

  <summary>Implementation</summary>

- store the elements of the matrix in an array of size rows \* cols
- sort the array
- store the elements from the array back to matrix
- Time Complexity is, $O(n^2logn)$
- Space Complexity is, $O(n^2)$

</details>

## Max Area under Histogram

<details>

  <summary>Implementation</summary>

- For every bar ‘x’, we calculate the area with ‘x’ as the smallest
  bar in the rectangle.
- If we calculate such area for every bar ‘x’ and find
  the maximum of all areas, our task is done. Now how to calculate area with ‘x’ as
  smallest bar? We need to know index of the first smaller (smaller than ‘x’)
  bar on left of ‘x’ and index of first smaller bar on right of ‘x’.
- We traverse all bars from left to right, maintain a stack of bars. Every bar is
  pushed to stack once.
- A bar is popped from stack when a bar of smaller height
  is seen. When a bar is popped, we calculate the area with the popped bar as
  smallest bar.
- How do we get left and right indexes of the popped bar – the
  current index tells us the ‘right index’ and index of previous item in stack
  is the ‘left index’.

- In his solution above current index is 'i' - which is the smallest bar index on the right of popped bar, and the index of smallest bar to the left of popped bar is the present top of stack which is stack.peek(). Hence the formula: (i - stack.peek() - 1).

- Time Complexity is, $O(n)$
- Space Complexity is, $O(n)$

</details>

## Max Area Rectangle

<details>

  <summary>Implementation</summary>

- take use of the max area under histogram algorithm
- traverse through the matrix and update matrix[i][j] with matrix[i-1][j]+matrix[i][j] if matrix[i][j] is not 0
- traverse through the last row and apply histogram method to find the max area
- Time Complexity is, $O(rows * cols)$
- Space Complexity is, $O(cols)$

</details>

## Find a specific pair in matrix

<details>

  <summary>Implementation</summary>

1. Use brute force method

   - Time Complexity is, $O(rows^2 * cols^2)$
   - Space Complexity is, $O(1)$

2. Matrix Pre-process method
   - create another max_matrix
   - pre process last col to contain the max el from that index to the last index
   - pre process last row to contain that max el from that index to the last index
   - continue the process will you reach start of the matrix, and update max value
   - enter value in the max_matrix by comparing the el itself, down and right
   - return max_value
   - Time Complexity is, $O(rows * cols)$
   - Space Complexity is, $O(rows * cols)$

</details>

## Rotate the matrix by 90deg

<details>

  <summary>Implementation</summary>

1. Using extra space

   - create a buffer matrix
   - convert,
   - first row of source -> last col of destination
   - second row of source -> second last col of destination
   - so ... on
   - last row of source -> first column of destination
   - change $destination[j][rows - 1 - i] = matrix[i][j]$ for 90deg
   - dimension changed from $(n * m) \rArr (m * n)$
   - Space Complexity is, $O(rows * cols)$
   - Time Complexity is, $O(rows * cols)$

2. For rotating 90deg -clockwise

   - find the transpose of the given matrix
   - reverse every rows of the matrix

3. For rotating 90deg -anticlockwise

   - find the transpose of the given matrix
   - reverse every column of the matrix

</details>
