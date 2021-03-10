# Array

**Table of Contents**

- [Array](#array)
  - [Reverse the Array](#reverse-the-array)
  - [Min Max in an Array](#min-max-in-an-array)
  - [Find the kth max/min element in an Array](#find-the-kth-maxmin-element-in-an-array)
  - [Given an array which consists of only 0, 1, and 2. Sort without using sorting algo](#given-an-array-which-consists-of-only-0-1-and-2-sort-without-using-sorting-algo)
  - [Move all the negative elements to one side of the array](#move-all-the-negative-elements-to-one-side-of-the-array)
  - [Find the Union and Intersection of the two sorted arrays.](#find-the-union-and-intersection-of-the-two-sorted-arrays)
  - [Write a program to cyclically rotate an array by one.](#write-a-program-to-cyclically-rotate-an-array-by-one)
  - [Find largest contiguous sum](#find-largest-contiguous-sum)
  - [Minimize the max difference b/w two heights](#minimize-the-max-difference-bw-two-heights)
  - [Minimum no. of jumps to reach end of an array](#minimum-no-of-jumps-to-reach-end-of-an-array)

---

## Reverse the Array

<details>

  <summary>Information</summary>

![](mdImages/2021-02-26-12-23-30.png)

- make two pointers, pointing to **start** and **end**
- swap elements in start and end with each other
- increment start and decrement end up until start is not greater than end

</details>

## Min Max in an Array

<details>

  <summary>Information</summary>

- There are three ways to do it

1. Linear Traversal, tracking max and min value and updating them respectively
2. Dividing the array into two halves and finding two max and two min.
   Comparing them and returning appropriate values.
3. Comparing them in pairs. If length of the array is odd, assign max and min to first and compare other items in pairs, else assign max and min to first two elements in the array and take a subsequent pair and compare them with the max and min and update them respectively.

</details>

## Find the kth max/min element in an Array

<details>

  <summary>Implementation</summary>

- Use Sorting and return the element in $O(logn)$ time
- Use MaxHeap/MinHeap method and pop elements to find kth element in $O(logn)$ time
- Use QuickSelect Method to find the element in worst case $O(n^2)$ but in average case $O(n)$ time

1. using QuickSelect paradigm to solve the problem,

- find the partition position
- find if the position is correct
- if position is greater than kth index, search in the left half
- otherwise, search in the right side

</details>

## Given an array which consists of only 0, 1, and 2. Sort without using sorting algo

<details>

  <summary>Implementation</summary>

- use three pointers, low, mid, high to demarcate the last index at which range of 0s, 1s, and 2s lies.
- iterate through the entire array and swap unknown values in their respective domain
- 0 to low will have values of 0s
- low = 0, mid = 0 and high = len(items) - 1
- if the element is 0 then swap the element at index low and update low = low + 1, and mid = mid + 1
- if the element is 1, update mid = mid + 1
- if the element is 2 then swap the element with element at high, and update high = high - 1 and update i = i - 1
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Move all the negative elements to one side of the array

<details>

  <summary>Implementation</summary>

> There are two methods

1. Use quick partition method to partition the array in linear time
2. Use two pointer method and swap the elements whenever it failed the constraints.

- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Find the Union and Intersection of the two sorted arrays.

<details>

  <summary>Implementation</summary>

> There are several ways to do that

1. Naive way of storing all first array elements and check the second array elements
   - Time Complexity is, $O(nm)$
1. Use of Hash
   - Time Complexity is, $O(n + m)$
1. Use of Map
   - Time Complexity is, $O(n + m)$
1. Use of Merge Operation
   - Time Complexity is, $O(n + m)$

</details>

## Write a program to cyclically rotate an array by one.

<details>

  <summary>Implementation</summary>

- cycle in array signifies the direction from left to right
- store last value in a variable
- shift all items in the array on position to the right from first to last(exclusive)
- store at first position the value that you've stored earlier
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Find largest contiguous sum

<details>

  <summary>Implementation</summary>

> There are two methods

1. Divide and Conquer

   - We can divide the array into three sections, whole array, left half, and right half
   - calculate the max contiguous subarray in each section and return the max value
   - Time Complexity is, $O(nlogn)$
   - Space Complexity is, $O(1)$

2. Kadane's Algorithm
   - The simple idea of Kadane's algorithm is to look for all positive contiguous segments of the array (max_ending_here is used for this).
   - And keep track of maximum sum contiguous segment among all positive segments (max_so_far is used for this)
   - Each time we get a positive-sum compare it with max_so_far and update max_so_far if it is greater than max_so_far
   - Time Complexity is, $O(n)$
   - Space Complexity is, $O(1)$

</details>

## Minimize the max difference b/w two heights

<details>

  <summary>Implementation</summary>

- Make an array of all possible heights > 0 using the value of k
- sort the array
- find the index upto which height of every tower is included from the starting. Initialize the answer to the difference between height at this index and starting index
- Then with the help of two pointer technique increment the left pointer which was initially at 0 such that one of the tower is not included
- Similarly increment right pointer to make all towers included and update the answer.
- Do this until end of the array
- Time Complexity is, $O(nlogn)$
- Space Complexity is, $O(n)$

</details>

## Minimum no. of jumps to reach end of an array

<details>

  <summary>Implementation</summary>

- We can use dynamic approach to solve this problem
- Time Complexity is, $O(nm)$
- Space Complexity is, $O(n)$

</details>
