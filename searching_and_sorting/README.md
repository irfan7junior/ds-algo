# Searching and Sorting

**Table of Contents**

- [Searching and Sorting](#searching-and-sorting)
  - [First and Last occurrences of X](#first-and-last-occurrences-of-x)
  - [Find a fix point (value equal to index) in a given array](#find-a-fix-point-value-equal-to-index-in-a-given-array)
  - [Search in a rotated sorted array](#search-in-a-rotated-sorted-array)
  - [Total count of numbers whose squares is less than the given number](#total-count-of-numbers-whose-squares-is-less-than-the-given-number)
  - [Max and Min in an array with Min comparisions](#max-and-min-in-an-array-with-min-comparisions)
  - [Optimum location of point to minimize total distance](#optimum-location-of-point-to-minimize-total-distance)
  - [Find the repeating and the missing](#find-the-repeating-and-the-missing)
  - [Find majority Element](#find-majority-element)
  - [Searching array adjacent differ k](#searching-array-adjacent-differ-k)
  - [Find a pair with a given difference](#find-a-pair-with-a-given-difference)
  - [Find four elements that sum to a given value](#find-four-elements-that-sum-to-a-given-value)
  - [Max sum such that no 2 elements are adjacent](#max-sum-such-that-no-2-elements-are-adjacent)
  - [Count triplets smaller than X](#count-triplets-smaller-than-x)
  - [Merge without extra space](#merge-without-extra-space)
  - [Print all subarrays with 0 sum](#print-all-subarrays-with-0-sum)
  - [Sort array according to count of set bits](#sort-array-according-to-count-of-set-bits)
  - [Product array puzzle](#product-array-puzzle)
  - [Minimum Swaps to sort](#minimum-swaps-to-sort)
  - [Bishu and Soldiers](#bishu-and-soldiers)
  - [Weighted Job Scheduling](#weighted-job-scheduling)
  - [Find pivot element in a sorted rotated array](#find-pivot-element-in-a-sorted-rotated-array)
  - [Find the inversion count](#find-the-inversion-count)
  - [Implementation of merge sort in-place](#implementation-of-merge-sort-in-place)

---

## First and Last occurrences of X

<details>

  <summary>Implementation</summary>

- Use binary search to find the index in $O(logn)$ time
- iterate left to find the left index
- iterate right to find the right index
- Space Complexity, $O(1)$
- Time Complexity, $O(n)$

</details>

## Find a fix point (value equal to index) in a given array

<details>

  <summary>Implementation</summary>

- traverse through the array
- check array[i] == i, return i
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Search in a rotated sorted array

<details>

  <summary>Implementation</summary>

- divide the array into two section, left sorted array and right sorted array
- initialize left = 0, right = len - 1, mid = (left + right) / 2
- while left <= right,
- check if the you're in the left sorted array, array[left] <= array[mid]
- check if array[mid] < target or check if array[left] > target, left = mid + 1
- else, right = mid - 1
- check if you're in the right sorted array, array[right] > array[mid]
- check if target < array[mid] or target > array[right], right = mid - 1
- else, left = mid + 1
- Time Complexity is, $O(logn)$
- Space Complexity is, $O(1)$

</details>

## Total count of numbers whose squares is less than the given number

<details>

  <summary>Implementation</summary>

- use binary search
- Time Complexity is, $O(logn)$
- Space Complexity is, $O(1)$

</details>

## Max and Min in an array with Min comparisions

<details>

  <summary>Implementation</summary>

- assign max and min using first item, if the len(array) is odd, otherwise with first two items
- iterate through the rest of the items
- if the current value is greater than max, update only max
- else, check if the current value is lesser than min, update only min
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Optimum location of point to minimize total distance

<details>

  <summary>Implementation</summary>

- we start with low and high initialized as some smallest and largest values respectively
- we start iteration, in each iteration we calculate two mids, mid1 and mid2, which represent 1/3rd and 2/3rd position in search space,
- we calculate total distance of all points with mid1 and mid2 and update low or high by comparing these
- iteration continues untill low and high become approximately equal
- Time Complexity is, $O(logn)$
- Space Complexity is, $O(1)$

</details>

## Find the repeating and the missing

<details>

  <summary>Implementation</summary>

1. Use of sorting

   - Time Complexity is, $O(nlogn)$
   - Space Complexity is, $O(1)$

2. Using auxiliary array
   - traverse through the array and mark the array as visited
   - if an element has already been marked, its the repeating element
   - traverse againt to find the missing element
   - Time Complexity is, $O(n)$
   - Space Complexity is, $O(n)$

</details>

## Find majority Element

<details>

  <summary>Implementation</summary>

- use hash_map,
- traverse through the array, increase the count of each key
- check if its count is greater than n/2
- return number
- Time Complexity is, $O(n)$
- Space Complexity is, $O(n)$

</details>

## Searching array adjacent differ k

<details>

  <summary>Implementation</summary>

- use the fact that array's el's value differ by k in the adjacent position
- traverse through the array, if x == target,
- (x - target)//k step away from the current index
- check again, return
- Time Complexity is, $O(1)$
- Space Complexity is, $O(1)$

</details>

## Find a pair with a given difference

<details>

  <summary>Implementation</summary>

- sort the array
- use two point method to find the given difference,
- left = 0, right = len - 1
- Time Complexity is, $O(nlogn)$
- Space Complexity is, $O(1)$

</details>

## Find four elements that sum to a given value

<details>

  <summary>Implementation</summary>

- use sorting as a preprocessing mechanism to reduce the time complexity
- use three nested loop to find the four elements which sums up to a given element
- Time Complexity is, $O(n^3)$
- Space Complexity is, $O(1)$

</details>

## Max sum such that no 2 elements are adjacent

<details>

  <summary>Implementation</summary>

- iterate through the array
- declare including and excluding
- calculate for each number greatest sum including and excluding the present number
- return max(including, excluding)
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Count triplets smaller than X

<details>

  <summary>Implementation</summary>

- use sorting
- for each element, use two pointer method to find the sum of the triplets
- increment count if sum is less than X
- Time Complexity is, $O(n^2)$
- Space Complexity is, $O(1)$

</details>

## Merge without extra space

<details>

  <summary>Implementation</summary>

- use two pointer method
- i = len(array1) and j = 0
- while i >= 0 and j < len(array2)
- if array1[i] >= array[2], swap these, i -= 1, j += 1
- finally, sort these two array
- Time Complexity is, $O((n + m) log(m + n))$
- Space Complexity is, $O(1)$

</details>

## Print all subarrays with 0 sum

<details>

  <summary>Implementation</summary>

- create a hash_table
- iterate through the array, initialize sum = 0 and result = []
- if sum + num is already present in hash_table, then
- for each key in hash_table, key + 1 till i are subarrays with total sum to zero
- Time Complexity is, $O(n)$
- Space Complexity is, $O(n)$

</details>

## Sort array according to count of set bits

<details>

  <summary>Implementation</summary>

- sort the elements based on the count of on bits present
- Time Complexity is, $O(nlogn)$
- Space Complexity is, $O(1)$

</details>

## Product array puzzle

<details>

  <summary>Implementation</summary>

- suppose $X = a*b*c*d$
- $logX = loga + logb + logc + logd$
- $answer[i] = antilog(logx - logi)$
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Minimum Swaps to sort

<details>

  <summary>Implementation</summary>

- store numbers position in hash_map
- sort the array and store in another array
- check if the ith number is sorted, if not increase count and replace the element both in array and hash_map
- Time Complexity is, $O(nlogn)$
- Space Complexity is, $O(n)$

</details>

## Bishu and Soldiers

<details>

  <summary>Implementation</summary>

- the array in already sorted
- find the greatest number less than equal to X
- sum the powers till that index
- return value
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Weighted Job Scheduling

<details>

  <summary>Implementation</summary>

- sort the jobs based on the early finish time
- create a recurring relation, find max profit including and excluding the current job
- memoize the solutions
- return the answer
- Time Complexity is, $O(n^2)$
- Space Complexity is, $O(n^2)$

</details>

## Find pivot element in a sorted rotated array

<details>

  <summary>Implementation</summary>

- we have to draw the graph and divide the array into two parts
- left sorted array, and right sorted array
- check if the array is even rotated or not, by nums[0] > nums[-1]
- use two pointer method to check for the anomaly, and return the value
- Time Complexity is, $O(logn)$
- Space Complexity is, $O(1)$

</details>

## Find the inversion count

<details>

  <summary>Implementation</summary>

- use merge sort technique to find out in nlogn time
- while merging process, if left[i] > right[j] that means mid - i elements need to be swapped
- Time Complexity is, $O(nlogn)$
- Space Complexity is, $O(n)$

</details>

## Implementation of merge sort in-place

<details>

  <summary>Implementation</summary>

- use the merge sort like you do normally
- in case of merging, do not create extra arrays
- instead check array[left] > array[right], then
- rotate the array to one unit to the right from left to mid
- increment left += 1, right += 1, mid += 1
- Time Complexity is, $O(n^2)$
- Space Complexity is, $O(1)$

</details>
