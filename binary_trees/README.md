# Binary Trees

- [Binary Trees](#binary-trees)
  - [Level Order Traversal](#level-order-traversal)
  - [Reverse Level Order Traversal](#reverse-level-order-traversal)
  - [Height of a tree](#height-of-a-tree)
  - [Find the diameter of a tree](#find-the-diameter-of-a-tree)
  - [Create a mirror tree](#create-a-mirror-tree)
  - [Inorder Traversal](#inorder-traversal)
  - [Preorder Traversal](#preorder-traversal)
  - [Postorder Traversal](#postorder-traversal)

## Level Order Traversal

<details>

  <summary>Implementation</summary>

- Creating a Binary Tree
- Apply Queue to print level order
- For printing each level in seperate lines use total_current_nodes and total_next_nodes

</details>

## Reverse Level Order Traversal

<details>

  <summary>Implementation</summary>

- use queue and stack to achieve it
- use queue to traverse level by level and stack to append it
- print stack.pop() while not empty
- Time Complexity is, $O(n)$
- Space Complexity is, $O(n)$

</details>

## Height of a tree

<details>

  <summary>Implementation</summary>

- max(left, right) + 1
- Time Complexity is, $O(n)$
- Space Complexity is, $O(height)$

</details>

## Find the diameter of a tree

<details>

  <summary>Implementation</summary>

- use recursion
- find the diameter in the left and right subtree
- find the diamter including the current root
- return the max of these
- Time Complexity is, $O(n^2)$
- Space Complexity is, $O(height)$

</details>

## Create a mirror tree

<details>

  <summary>Implementation</summary>

- use recursion
- if root == None, return None
- create a mirror = new_node(root.value)
- mirror.right = mirrorify(root.left, mirror.right)
- mirror.left = mirrorify(root.right, mirror.left)
- return mirror
- Time Complexity is, $O(n)$
- Space Complexity is, $O(height)$

</details>

## Inorder Traversal

<details>

  <summary>Implementation</summary>

- left, print(parent), right
- use recursion
- or stack
- non-decreasing order in case of binary search tree
- Time Complexity is, $O(n)$
- Space Complexity is, $O(height)$
  ![](mdImages/2021-03-29-13-45-53.png)

</details>

## Preorder Traversal

<details>

  <summary>Implementation</summary>

- print(parent), recur left, recur right
- use recursion
- use stack
- Time Complexity is, $O(n)$
- Space Complexity is, $O(height)$
  ![](mdImages/2021-03-29-13-59-39.png)

</details>

## Postorder Traversal

<details>

  <summary>Implementation</summary>

- recur left, recur right, print(parent)
- use recursion
- use two stack method
- print the second stack
- Time Complexity is, $O(n)$
- Space Complexity is, $O(n)$

</details>
