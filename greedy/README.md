# Greedy

- [Greedy](#greedy)
  - [Activity Selection Problem](#activity-selection-problem)

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
