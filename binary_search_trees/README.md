# Binary Search Trees

- [Binary Search Trees](#binary-search-trees)
  - [Find a value in a BST](#find-a-value-in-a-bst)
  - [Delete a node in the Binary Search Tree](#delete-a-node-in-the-binary-search-tree)
  - [Find min and max in a BST](#find-min-and-max-in-a-bst)
  - [Inorder successor and Inorder predecessor in BST](#inorder-successor-and-inorder-predecessor-in-bst)
  - [Check for BST](#check-for-bst)
  - [Populate inorder successor for all nodes](#populate-inorder-successor-for-all-nodes)
  - [Lowest Common Ancestor](#lowest-common-ancestor)
  - [Construct BST from given preorder traversal](#construct-bst-from-given-preorder-traversal)
  - [Convert Binary Tree to Binary Search Tree](#convert-binary-tree-to-binary-search-tree)
  - [BST to Balanced BST](#bst-to-balanced-bst)
  - [Find Kth largest element in a BST](#find-kth-largest-element-in-a-bst)
  - [Find Kth smallest element in a BST](#find-kth-smallest-element-in-a-bst)

## Find a value in a BST

<details>

  <summary>Implementation</summary>

- Build a Binary Search Tree
- Do a iterative search, find the element and return the node
- Do a recursive search, find the element and return the node

</details>

## Delete a node in the Binary Search Tree

<details>

  <summary>Implementation</summary>

- There are total 4 cases to consider
- when it is leaf node
- when it doesn't have left child or right child
- when inorder successor is its right child
- when inorder successor is not its right child
- use transplant as a sub-procedure to simplify the operation
- Time Complexity is, $O(logn)$
- Space Complexity is, $O(logn)$

</details>

## Find min and max in a BST

<details>

  <summary>Implementation</summary>

- for min, travel node.left until None
- for max, travel node.right until None
- Time Complexity is, $O(logn)$
- Space Complexity is, $O(1)$

</details>

## Inorder successor and Inorder predecessor in BST

<details>

  <summary>Implementation</summary>

- if root is null, return
- if key if found,

  - if its left subtree is not null, then predecessor will be the right most child of left subtree or left child itself
  - if its right subtree is not null the successor will be the left most child of right subtree or right child itself

- if key is smaller then root node
  - set sucessor as root
  - search recursively into left subtree
  - else,
  - set predecessor as root
  - search recursively into right subtree

</details>

## Check for BST

<details>

  <summary>Implementation</summary>

- use inorder traversal to find that the elements are in non-decreasing order
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Populate inorder successor for all nodes

<details>

  <summary>Implementation</summary>

- do a inorder traversal
- use a pointer to mark the previous pointer
- change prev.next = current
- Time Complexity is, $O(n)$
- Space Complexity is, $O(logn)$s

</details>

## Lowest Common Ancestor

<details>

  <summary>Implementation</summary>

- if the current.value is less than both the nodes' values, search in the right subtree
- if the current.value is greater than both the nodes' values, search in the left subtree
- return the current node, as lcs
- Time Complexity is, $O(logn)$
- Space Complexity is, $O(1)$

</details>

## Construct BST from given preorder traversal

<details>

  <summary>Implementation</summary>

- use MIN, MAX method to find out the node to insert
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Convert Binary Tree to Binary Search Tree

<details>

  <summary>Implementation</summary>

- store the nodes in the inorder traversal in an array
- sort the array
- inorder traversal and put the element from array to binary tree
- Time Complexity is, $O(nlogn)$
- Space Complexity is, $O(n)$

</details>

## BST to Balanced BST

<details>

  <summary>Implementation</summary>

- store elements from inorder traversal of bst in an array
- find the middle element, make it the root and recur for the left half and right half
- Time Complexity is, $O(n)$
- Space Complexity is, $O(n)$

</details>

## Find Kth largest element in a BST

<details>

  <summary>Implementation</summary>

- do a reverse inorder traversal
- Time Complexity is, $O(n)$
- Space Complexity is, $O(logn)$

</details>

## Find Kth smallest element in a BST

<details>

  <summary>Implementation</summary>

- do an inorder traversal
- Time Complexity is, $O(n)$
- Space Complexity is, $O(logn)$

</details>
