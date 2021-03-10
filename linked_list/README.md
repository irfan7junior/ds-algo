# Linked List

- [Linked List](#linked-list)
  - [Write a program to reverse a Linked List](#write-a-program-to-reverse-a-linked-list)

## Write a program to reverse a Linked List

<details>

  <summary>Implementation</summary>

- make three pointers, cur, left, and right
- iterate while cur is not None
- in each iteration,
  - change right to cur.right
  - change cur.right to prev
  - change prev to cur
  - change cur to right
- Time Complexity, $O(n)$
- Space Complexity, $O(1)$

</details>
