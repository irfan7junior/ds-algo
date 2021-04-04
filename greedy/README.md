# Greedy

- [Greedy](#greedy)
  - [Activity Selection Problem](#activity-selection-problem)
  - [Job Sequencing Problem](#job-sequencing-problem)
  - [Huffman Tree coding](#huffman-tree-coding)
  - [Fractional Knapsack Problem](#fractional-knapsack-problem)
  - [Permutation of a string](#permutation-of-a-string)
  - [Maximum Trains Stoppage can be provided](#maximum-trains-stoppage-can-be-provided)
  - [Minimum Platforms](#minimum-platforms)
  - [Buy Max stocks with ith at most stack can be bought](#buy-max-stocks-with-ith-at-most-stack-can-be-bought)
  - [Shop in candy store](#shop-in-candy-store)
  - [Minimize cash flow among given set of friends borrowed money](#minimize-cash-flow-among-given-set-of-friends-borrowed-money)

## Activity Selection Problem

<details>

  <summary>Implementation</summary>

> There is one meeting room in a firm. There are N meetings in the form of (**S[i]**, **F[i]**) where **S[i]** is start time of meeting i and **F[i]** is finish time of meeting i.
> What is the **maximum** number of meetings that can be accommodated in the meeting room when only one meeting can be held in the meeting room at a particular time? Also not start time of one chosen meeting can't be equal to the end time of the other chosen meeting.

- Some standard algorithms that are Greedy algorithms

  1. **Krushkal's Minimum Spanning Tree (MST)**
  2. **Prim's Minimum Spanning Tree**
  3. **Dijkstra's Shortest Path**
  4. **Huffman Coding**

- The greedy choice is to always pick the next activity whose finish time is least among the remaining activities and the start time is more than the finish time of the previously selected activity
- Sort the activities according to their finishing time
- Select the first activity from the sorted array and print it
- Do the following for the remaining activities in the sorted array.
  - If the start time of this activity is greater than or equal to the finish time of previously selected activity then select this activity and print it.

</details>

## Job Sequencing Problem

<details>

  <summary>Implementation</summary>

- sort the jobs based on the non-decreasing profit
- iterate through the jobs and for each job find the farthest time, you could do the job
- do the job there
- Time Complexity is, $O(n*m)$
- Space Complexity is, $O(m)$

</details>

## Huffman Tree coding

<details>

  <summary>Implementation</summary>

- use priority queue, heap to store the node values with their frequencies
- extract top two nodes and make a frequency root node
- assign left child to the node having small frequency value
- assign right child to the node having big frequency value
- Time Complexity is, $O(nlogn)$
- Space Complexity is, $O(n)$

</details>

## Fractional Knapsack Problem

<details>

  <summary>Implementation</summary>

- find the profit/weight and sort them
- find the total profit under the weight
- Time Complexity is, $O(nlogn)$
- Space Complexity is, $O(1)$

</details>

## Permutation of a string

<details>

  <summary>Implementation</summary>

- iterate through the characters
- replace it with first characters
- call permutation on the remaining characters
- recur
- Time Complexity is, $O(n^n)$
- Space Complexity is, $O(n)$

</details>

## Maximum Trains Stoppage can be provided

<details>

  <summary>Implementation</summary>

- sort the trains wrt the departure time
- check if the platforms are available
- fill that platform, increase train count
- clear the platform if time it is allowed to do so
- Time Complexity is, $O(nlogn)$
- Space Complexity is, $O(1)$

</details>

## Minimum Platforms

<details>

  <summary>Implementation</summary>

- sort the arrival time and departure time
- iterate through both the array, and check
- if arrival[i] <= departure[j], max++, result = maximum(max, result), else max--
- Time Complexity is, $O(nlogn)$
- Space Complexity is, $O(1)$

</details>

## Buy Max stocks with ith at most stack can be bought

<details>

  <summary>Implementation</summary>

- sort the array first by less stock price then by more day
- traverse and find the max stocks that can be bought
- Time Complexity is, $O(nlogn)$
- Space Complexity is, $O(1)$

</details>

## Shop in candy store

<details>

  <summary>Implementation</summary>

- sort the prices of candies in non-decreasing order
- select the lowest price candy
- select k candies from the right side
- buy the remaining ones with money
- return total money
- Time Complexity is, $O(nlogn)$
- Space Complexity is, $O(1)$

</details>

## Minimize cash flow among given set of friends borrowed money

<details>

  <summary>Implementation</summary>

- find the total negative or positive cash flow for each friend
- sort the array
- left = array[0], right = array[-1]
- while left != right:
- if min(abs(left), abs(right)) = left, friend[left] pays left amount to friend[right], left += 1
- if min(abs(left), abs(right)) = right, frient[left] pays right amount to friend[right], right -= 1
- Time Complexity is, $O(n^2)$
- Space Complexity is, $O(n)$

</details>
