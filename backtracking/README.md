# Backtracking

- [Backtracking](#backtracking)
  - [Rat in a Maze](#rat-in-a-maze)

## Rat in a Maze

> Consider a rat placed at **(0, 0)** in a square matrix of order **N \* N**. It has to reach the destination at **(N - 1, N - 1)**. Find all possible paths that the rat can take to reach from source to destination. The directions in which the rat can move are **'U'(up), 'D'(down), 'L'(left), 'R'(right)**.
> Value 0 at a cell in the matrix represents that it is blocked and rat cannot move to it while value 1 at a cell in the matrix representss that rat can be travel through it.
> **Note**: In a paht, no cell can be visited more than one time.

- Start from the initial index (0, 0) and look for the valid moves through the adjacent cells in the order **Down -> Left -> Right -> Up**
- If the move is possible, then move to that cell while storing the character corresponding to the move (D, L, R, U) and again start looking for the valid move until the last index (n-1, n-1) is reached.
- Also, keep on marking the cells as visited and when we traversed all the paths possible from that cell, then unmark that cell for other different paths and remove the character from the path formed.
- As the last index of the grid (bottom right) is reached, the store the traversed path.
- Time Complexity, $O(3^{n^2})$, as there are $O(n^2)$ cells from each cell there are 3 unvisited neighbouring cells.
- Space Complexity, $O(3^{n^2})$, as there can be atmost that many cells in the answer.
