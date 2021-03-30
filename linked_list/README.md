# Linked List

- [Linked List](#linked-list)
  - [Write a program to reverse a Linked List](#write-a-program-to-reverse-a-linked-list)
  - [Reverse a Linked List in groups of given size](#reverse-a-linked-list-in-groups-of-given-size)
  - [Detect a loop in a linked list](#detect-a-loop-in-a-linked-list)
  - [Delete a loop in a linked list](#delete-a-loop-in-a-linked-list)
  - [Starting point of a loop in a linked list](#starting-point-of-a-loop-in-a-linked-list)
  - [Remove Duplicates in a sorted Linked List](#remove-duplicates-in-a-sorted-linked-list)
  - [Remove Duplicates in a un-sorted linked list](#remove-duplicates-in-a-un-sorted-linked-list)
  - [Move the last element to front in a linked list](#move-the-last-element-to-front-in-a-linked-list)
  - [Add a number represented as a linked list](#add-a-number-represented-as-a-linked-list)
  - [Add two numbers represented by linked list](#add-two-numbers-represented-by-linked-list)
  - [Intersection of two linked list](#intersection-of-two-linked-list)
  - [Intersection Pointer of two joint linked list](#intersection-pointer-of-two-joint-linked-list)

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

## Reverse a Linked List in groups of given size

<details>

  <summary>Implementation</summary>

- use stack to store the elements in the reverse order
- initialize, prev = Null and current = ll.head
- while current is not None,
- reverse the link
- for prev = None, ll.head = prev
- Time Complexity is, $O(n)$
- Space Complexity is, $O(k)$

</details>

## Detect a loop in a linked list

<details>

  <summary>Implementation</summary>

- use floyd's algorithm for tortoise and hare problem
- create hare which would traverse till hare.next is not None,
- create tortoise which would traverse till tortoise is not None,
- if both of them met and have same value, return that link
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Delete a loop in a linked list

<details>

  <summary>Implementation</summary>

- use floyd's algorithm and tortoise and hare method
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Starting point of a loop in a linked list

<details>

  <summary>Implementation</summary>

- use floyd's algorithm
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Remove Duplicates in a sorted Linked List

<details>

  <summary>Implementation</summary>

- create two pointers, first = ll.head, second = first.right
- while first is not None,
- while second is not None and second.value == first.value
- finally, first.right = second, first = second, second = first.right
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Remove Duplicates in a un-sorted linked list

<details>

  <summary>Implementation</summary>

- use sorting
- use two loops
- use hashing
  - Time Complexity is, $O(n)$
  - Space Complexity is, $O(n)$

</details>

## Move the last element to front in a linked list

<details>

  <summary>Implementation</summary>

- use iteration method
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Add a number represented as a linked list

<details>

  <summary>Implementation</summary>

- reverse the linked list
- add the number using carry method
- reverse the linked list again
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Add two numbers represented by linked list

<details>

  <summary>Implementation</summary>

- reverse both the linked list
- do carry based addition with two linked list
- store the result into the new linked list
- Time Complexity is, $O(n)$
- Space Complexity is, $O(n)$

</details>

## Intersection of two linked list

<details>

  <summary>Implementation</summary>

- iterate through both the linked list with two pointers
- if both the elements are same, increment both the pointers
- if they are different, add the smallest element and increment its pointer
- Time Complexity is, $O(n + m)$
- Space Complexity is, $O(n + m)$

</details>

## Intersection Pointer of two joint linked list

<details>

  <summary>Implementation</summary>

- count the length2 and length1
- traverse till length-length times in bigger linked list
- now, traverse one node at a time till we find the common point
- return that value
- Time Complexity is, $O(n+m)$
- Space Complexity is, $O(1)$

</details>
