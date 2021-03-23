# String

**Table of Contents**

- [String](#string)
  - [Reverse a String](#reverse-a-string)
  - [Check palindrome](#check-palindrome)
  - [Print all the duplicates in string](#print-all-the-duplicates-in-string)
  - [Why are strings immutable in java](#why-are-strings-immutable-in-java)
  - [Write a code to check whether one string is a rotation of another](#write-a-code-to-check-whether-one-string-is-a-rotation-of-another)
  - [Check if a string is a valid shuffle of two other strings](#check-if-a-string-is-a-valid-shuffle-of-two-other-strings)
  - [Count and say](#count-and-say)
  - [Longest Palindrome in a string](#longest-palindrome-in-a-string)
  - [Longest Common Subsequence](#longest-common-subsequence)
  - [Longest Recurring Subsequence](#longest-recurring-subsequence)
  - [Print all Substring](#print-all-substring)
  - [Print all Permutations](#print-all-permutations)
  - [Count the Binary strings into two substring with equal 0's and 1's](#count-the-binary-strings-into-two-substring-with-equal-0s-and-1s)
  - [Word Wrap Problem](#word-wrap-problem)
  - [Edit Distance](#edit-distance)
  - [Next Greater Permutation](#next-greater-permutation)
  - [Balance Parenthesis](#balance-parenthesis)
  - [Word Break Problem](#word-break-problem)
  - [Robin Karp Substring search (Rolling Hash Method)](#robin-karp-substring-search-rolling-hash-method)
  - [KMP Substring Search](#kmp-substring-search)
  - [Convert a Sentence into its equivalent mobile numerical keypad sequence](#convert-a-sentence-into-its-equivalent-mobile-numerical-keypad-sequence)
  - [Minimum Bracket Reversals](#minimum-bracket-reversals)
  - [Count Palindromic Subsequences](#count-palindromic-subsequences)
  - [Search a Word in a 2d grid of characters](#search-a-word-in-a-2d-grid-of-characters)
  - [Count of Word in a Matrix](#count-of-word-in-a-matrix)
  - [Convert Roman Numerals to Decimal](#convert-roman-numerals-to-decimal)
  - [Longest Common Prefix of strings](#longest-common-prefix-of-strings)
  - [Minimum Number of flips to make binary string alternate](#minimum-number-of-flips-to-make-binary-string-alternate)
  - [Find the second-most repeated word in string](#find-the-second-most-repeated-word-in-string)
  - [Longest Common Subsequence](#longest-common-subsequence-1)
  - [Generate all possible valid IP addresses from given string](#generate-all-possible-valid-ip-addresses-from-given-string)
  - [Smallest Window that contains all the characters of the string](#smallest-window-that-contains-all-the-characters-of-the-string)
  - [Minimum Character added at the front to make the string palindrome](#minimum-character-added-at-the-front-to-make-the-string-palindrome)
  - [Print all the anagrams together, given words array](#print-all-the-anagrams-together-given-words-array)
  - [Smallest window in a string containing all the characters of another string](#smallest-window-in-a-string-containing-all-the-characters-of-another-string)
  - [Recurisvely remove all adjacent duplicates](#recurisvely-remove-all-adjacent-duplicates)
  - [Transform one string to another using min. swap to front](#transform-one-string-to-another-using-min-swap-to-front)

---

## Reverse a String

<details>

  <summary>Implementation</summary>

- use start pointer and end pointers
- while start <= end, interchange values at string[start] and string[end] with each other
- Space Complexity, $O(1)$
- Time Complexity, $O(length)$

</details>

## Check palindrome

<details>

  <summary>Implementation</summary>

- use two pointer method
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Print all the duplicates in string

<details>

  <summary>Implementation</summary>

- use hash or map to find the number of occurences of each char in the string
- iterate throught the hash or map values
- print char whose occurences are more than 1
- Time Complexity is, $O(n)$
- Space Complexity is, $O(n)$

</details>

## Why are strings immutable in java

<details>

  <summary>Answer</summary>

- it makes the string thread safe since they won't be changed when accessed from multiple threads.
- Caching the String literals and reusing them saves a lot of heap space because different String variables refer to the same object in the String pool. String intern pool serves exactly this purpose.
- The immutability guarantees Strings that their value won’t change. So the hashCode() method is overridden in String class to facilitate caching, such that the hash is calculated and cached during the first hashCode() call and the same value is returned ever since.

</details>

## Write a code to check whether one string is a rotation of another

<details>

  <summary>Implementation</summary>

- create a temp = string1 + string1 (cdabcdab)
- find whether string2 is a substring in temp
- Time Complexity is, $O(n + m)$
- Space Complexity is, $O(n)$

</details>

## Check if a string is a valid shuffle of two other strings

<details>

  <summary>Implementation</summary>

- i = j = k = 0
- start iterating the resultant string
- if check string1[i] == result[k], increment i
- elif check string2[j] == result[k], increment j
- else, return False
- finally, increment k
- Time Complexity is, $O(len(string1) + len(string2))$
- Space Complexity is, $O(1)$

</details>

## Count and say

<details>

  <summary>Implementation</summary>

- iterate through the string, prevChar = string[0], count = 1
- check if the currentChar != preChar, append(count + prevChar)
- else, count += 1
- outside, append(count + prevChar)
- return result
- Time Complexity is, $O(n)$
- Space Complexity is, $O(n)$

</details>

## Longest Palindrome in a string

<details>

  <summary>Implementation</summary>

- if length == 1, return true
- if length == 2, check and return true or false
- sub(i, j) -> if str[i] == str[j] and dp[i+1][j-1] == 1, return true
- return false
- Time Complexity is, $O(n^2)$
- Space Complexity is, $O(n^2)$

</details>

## Longest Common Subsequence

<details>

  <summary>Implementation</summary>

- create a memo table (len(string1) + 1) \* (len(string2) + 1)
- initialize the phie values with 0
- for each i, j check whether string1[i][j] == string2[i][j] matches,
- set memo[i][j] = memo[i-1][j-1] + 1
- else, set memo[i][j] = max(memo[i-1][j], memo[i][j-1])
- return memo[-1][-1]
- Time Complexity is, $O(n^2)$
- Space Complexity is, $O(n^2)$

</details>

## Longest Recurring Subsequence

<details>

  <summary>Implementation</summary>

- The idea is same as the longest commong subsequence
- but we have to ignore the case whether string1[i] == string2[j] and i == j
- Time Complexity is, $O(n^2)$
- Space Complexity is, $O(n^2)$
</details>

## Print all Substring

<details>

  <summary>Implementation</summary>

- use recursion
- for each node, if input is empty, print output
- else, recur, adding and not adding the first element
- Time Complexity is, $O(2^n)$
- Space Complexity is, $O(n)$

</details>

## Print all Permutations

<details>

  <summary>Implementation</summary>

- iterate throught start and end
- and swap string[i] with string[start]
- permutate(string, start + 1, end)
- swap string[i] with string[start]
- if start == end, print(string)
- Time Complexity is, $O(n! * n)$
- Space Complexity is, $O(n)$

</details>

## Count the Binary strings into two substring with equal 0's and 1's

<details>

  <summary>Implementation</summary>

- initialize, count_0, count_1, count as 0
- iterate through the char in string,
- if char == '0', increment count_0
- elif char == '1', increment count_1
- finally, if count_0 == count_1, increment count
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Word Wrap Problem

<details>

  <summary>Implementation</summary>

- formula is, M[i] = min (j == i+1...len) { m[j] + c[i][j-1] }
- create a cost matrix
- iterate through it with the help to one dimensional array to get the result
- Time Complexity is, $O(n^2)$
- Space Complexity is, $O(n^2)$

</details>

## Edit Distance

<details>

  <summary>Implementation</summary>

- if $str1[i] == str2[j], T[i, j] = T[i-1, j-1]$
- else, $T[i, j] = min(T[i-1, j-1], T[i-1, j], T[i, j-1]) + 1$
- Time Complexity is, $O(n^2)$
- Space Complexity is, $O(n^2)$

</details>

## Next Greater Permutation

<details>

  <summary>Implementation</summary>

- iterate through the right side of the array
- find the index of the element which is greater than the previously traversed digit
- swap that digit with the rightmost digit
- sort (i + 1, last) or reverse (i + 1, last)
- you get the next permutation
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Balance Parenthesis

<details>

  <summary>Implementation</summary>

- create a stack, openB = [ '(', '{', '[' ], closeB = [ ')', '}', ']' ]
- traverse through the string, char = string[i]
- check char in openB, then push char in stack
- check char in closeB, then pop top, check top matches closing char, if true continue, else return false
- if neither char in openB or closeB, continue
- after traversing, if len(stack) != 0, return false
- Time Complexity is, $O(n)$
- Space Complexity is, $O(n)$

</details>

## Word Break Problem

<details>

  <summary>Implementation</summary>

- for i in range(len(string))
- return any([(word[:i] in wordList) and wordBreak(wordList, word[i:]) for i in range(1, wordLen+1)])
- if word == '', return True
- Time Complexity is, $O(n^2)$
- Space Complexity is, $O(n)$

</details>

## Robin Karp Substring search (Rolling Hash Method)

<details>

  <summary>Implementation</summary>

- calculate the hash for the pattern
- roll the text substring to find hash value, and compare it with pattern's
- return index
- Time Complexity is, $O(n + m)$
- Space Complexity is, $O(1)$

</details>

## KMP Substring Search

<details>

  <summary>Implementation</summary>

- build a substring array to store the values of same prefix and suffix indices
- traverse through the text and find the index of the match using substring array
- Time Complexity is, $O(n + m)$
- Space Complexity is, $O(m)$

</details>

## Convert a Sentence into its equivalent mobile numerical keypad sequence

<details>

  <summary>Implementation</summary>

- add a dictionary storing the map between the characters and count \* number
- iterate through string, and print the value store in the dict for each map
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Minimum Bracket Reversals

<details>

  <summary>Implementation</summary>

- create a stack, iterate through the parens
- push open parens, pop a open parens for a close parens
- count the number of open parens and close parens in the stack
- ceil divide both of them by 2 and add them
- Time Complexity is, $O(n)$
- Space Complexity is, $O(n)$

</details>

## Count Palindromic Subsequences

<details>

  <summary>Implementation</summary>

- create a matrix for storing boolean values
- fill tables in $O(n^2)$ time
- count total boolean values in the matrix
- return total
- Time Complexity is, $O(n^2)$
- Space Complexity is, $O(n^2)$

</details>

## Search a Word in a 2d grid of characters

<details>

  <summary>Implementation</summary>

- create a direction array
- traverse through each cell in the matrix
- check the presence of the search_text starting from this cell in all direction
- return True if found
- return False if no match is found
- Time Complexity is, $O(n * m * k)$
- Space Complexity is, $O(1)$

</details>

## Count of Word in a Matrix

<details>

  <summary>Implementation</summary>

- Recursive traverse in all the given direction
- add value of found
- return found
- Time Complexity is, $O(n * m * k)$
- Space Complexity is, $O(1)$

</details>

## Convert Roman Numerals to Decimal

<details>

  <summary>Implementation</summary>

- map the roman digits to its decimal values
- iterate through the roman numeral digits
- check if the current roman digit is greater than the next digit
- if not, subtract the mapped next digit with the current mapped digit and add to the sum
- if true, just add the mapped current roman digit to the sum
- return sum
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Longest Common Prefix of strings

<details>

  <summary>Implementation</summary>

- find the length of smallest string in the array
- start from 0 till the point where either the smallest string has been completely traversed
- or there is a point of difference
- return the length
- Time Complexity is, $O(n*m)$
- Space Complexity is, $O(1)$

</details>

## Minimum Number of flips to make binary string alternate

<details>

  <summary>Implementation</summary>

- need to traverse through the string two times
- take the minimum of these two
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>

## Find the second-most repeated word in string

<details>

  <summary>Implementation</summary>

- tokenize each word using hashmap and increase the count
- traverse again to find the second-most repeated word
- Time Complexity is, $O(n)$
- Space Complexity is, $O(n)$

</details>

## Longest Common Subsequence

<details>

  <summary>Implementation</summary>

- find the cost matrix
- if X[m-1] == Y[n-1], return 1 + lcs(X, Y, m-1, n-1)
- else, return max(lcs(X, Y, m, n-1), lcs(X, Y, m-1, n))
- Time Complexity is, $O(n*m)$
- Space Complexity is, $O(n*m)$

</details>

## Generate all possible valid IP addresses from given string

<details>

  <summary>Implementation</summary>

- create is_valid function to check whether and IP address is correct
- create three loops to iterate over to find all the ip address
- check them with the help of is_valid and append them to the result
- Time Complexity is, $O(n^3)$
- Space Complexity is, $O(n^3)$

</details>

## Smallest Window that contains all the characters of the string

<details>

  <summary>Implementation</summary>

- use sliding window technique
- find the total length of set of distinct characters
- create a hash_map to store the frequence of each distinct key
- initialize count = 0, start = 0, min_length = length(string)
- for (i, char) in enumerate(string),
- increment the frequence of char in hash_map by 1
- pass if frequence of char currently is 1 but increment count
- check count == len(distinct_set),
- iterate check string[start]'s frequence is > 1, do
- reduce it's frequency, increment start, check new_window length and update it respectively
- Time Complexity is, $O(n)$
- Space Complexity is, $O(n)$

</details>

## Minimum Character added at the front to make the string palindrome

<details>

  <summary>Implementation</summary>

- final_string = ''
- concat final_string, string + '$' + reversed(string)
- find the prefix_array for final_string used in KMP algorithm
- return len(final_string) - prefix_array[-1]
- Time Complexity is, $O(n)$
- Space Complexity is, $O(n)$

</details>

## Print all the anagrams together, given words array

<details>

  <summary>Implementation</summary>

1. Use hash_map to store the words which have similar hash value
2. Use of two auxillary array

</details>

## Smallest window in a string containing all the characters of another string

<details>

  <summary>Implementation</summary>

- use sliding window technique
- create a hash_map, total_count = set(text2), count = 0, min_length = len(text1)
- minimize min_length using sliding window
- Time Complexity is, $O(n)$
- Space Complexity is, $O(m)$

</details>

## Recurisvely remove all adjacent duplicates

<details>

  <summary>Implementation</summary>

- use recursion
- base case, when len(string) == index, return ''
- if prev_char == cur_char, skip cur_char, recursive call
- else, print cur_char, recursive call
- Time Complexity is, $O(n)$
- Space Complexity is, $O(n)$

</details>

## Transform one string to another using min. swap to front

<details>

  <summary>Implementation</summary>

- check the frequencies between two strings
- initialize i = len1, j = len2, count = 0
- while i >= 0,
- if text1[i] == text2[j], i -= 1, j-= 1
- else, while text1[i] != text2[j], i -= 1, result += 1
- i -= 1, j -= 1
- return count
- Time Complexity is, $O(n)$
- Space Complexity is, $O(1)$

</details>
