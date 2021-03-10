# Bit Manipulation

- [Bit Manipulation](#bit-manipulation)
  - [Count set bits in an integer](#count-set-bits-in-an-integer)

## Count set bits in an integer

<details>

  <summary>Implementation</summary>

- Use logarithm approach to divide the value by 2
- if the modulus is 1, increment the value of count
- divide the value by 2 and floor the result
- continue till value != 0
- return count
- Time Complexity is, $O(logn)$
- Space Complexity is, $O(1)$

</details>
