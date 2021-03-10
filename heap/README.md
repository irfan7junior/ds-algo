# Heap

- [Heap](#heap)
  - [Implement a MaxHeap / MinHeap using arrays and recursion](#implement-a-maxheap--minheap-using-arrays-and-recursion)

## Implement a MaxHeap / MinHeap using arrays and recursion

<details>

  <summary>Implementation</summary>

- create a Heap class
- items attribute would have one extra None element to counter the 1 offset due to 0 based array indexing
- parent = index // 2
- left = index \* 2
- right = index \* 2 + 1
- implement heapify for an index
- implement build_heap using heapify from (len(items) - 1) // 2 to 1

</details>
