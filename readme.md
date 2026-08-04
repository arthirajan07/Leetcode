# Day 1
PROBLEM STATEMENT: Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target. You may assume that each input would have exactly one solution, and you may not use the same element twice.

DESCRIPTION: The twoSum function finds the indices of two numbers in the given array nums whose sum is equal to the given target. It uses a brute-force approach by checking every possible pair of elements in the array. If a pair whose sum equals the target is found, the function immediately returns their indices. If no such pair exists, it returns an empty vector.

ALGORITHM: STEP 1: Start from the first element of the array. STEP 2: Compare it with every element that comes after it. STEP 3: Add the two elements. STEP 4: If their sum is equal to the target, return their indices. STEP 5: If not, continue checking the next pair. STEP 6: Repeat this process until a matching pair is found. STEP 7: If no pair is found after checking all possible pairs, return an empty vector {}.
--------------------------------------------------------------------------------------
# Day 2 - Add Two Numbers
Description:
This solution traverses both linked lists simultaneously and adds corresponding digits along with any carry from the previous addition. A dummy node is used to simplify the creation of the result linked list. The process continues until all digits and any remaining carry are processed.

Algorithm:
Step 1: Create a dummy node to store the result.
Step 2: Initialize a pointer `current` to the dummy node and set `carry = 0`.
Step 3: Traverse both linked lists while either list has nodes or carry exists.
Step 4: Extract values from the current nodes (use 0 if a list has ended).
Step 5: Compute the sum of both values and carry.
Step 6: Store the digit `(sum % 10)` in a new node.
Step 7: Update carry as `(sum // 10)`.
Step 8: Move to the next nodes in both linked lists.
Step 9: Return the linked list starting from `dummy.next`.
--------------------------------------------------------------------------------------
# Day 3

Problem Statement:
Given a string `s`, find the length of the longest substring without repeating characters.

Approach:
Used the Sliding Window technique with a Hash Set to maintain unique characters within the current window. If a duplicate character is found, the left pointer moves forward until the duplicate is removed.

Algorithm:
1. Initialize an empty set.
2. Use two pointers (`left` and `right`) to represent the sliding window.
3. Expand the window by moving `right`.
4. If a duplicate character is found, shrink the window from the left.
5. Update the maximum length found.
6. Return the maximum length.
--------------------------------------------------------------------------------------
# Day 4 - Median of Two Sorted Arrays
DESCRIPTION: 
      Given two sorted arrays nums1 and nums2 of size m and n respectively, return the median of the two sorted arrays.

ALGORITHM:
    1. Merge nums1 and nums2.
    2.Sort the merged array.
    3.Find the total number of elements.
    4.If the count is odd, return the middle element.
    5.If the count is even, return the average of the two middle elements.  
---------------------------------------------------------------------------------------

# Day 5 - Longest Palindromic Substring
Problem Statement:
Given a string `s`, return the longest palindromic substring in `s`.

Approach:
Used the **Expand Around Center** technique. Consider each character as the center of a palindrome, expand in both directions for odd and even length palindromes, and keep track of the longest substring found.

Algorithm:
1. Initialize an empty string `res`.
2. Traverse each character in the string.
3. Expand around the current index for odd-length palindrome.
4. Expand around the gap between current and next index for even-length palindrome.
5. Update `res` if a longer palindrome is found.
6. Return the longest palindromic substring.
-----------------------------------------------------------------------------------------

# Day 6 - Zigzag Conversion

Description:
Given a string `s` and an integer `numRows`, arrange the string in a zigzag pattern and return the string read row by row.
Approach:
- Create a list for each row.
- Traverse the string character by character.
- Move downward through the rows, then upward.
- Append each character to the corresponding row.
- Join all rows to get the final result.

 Algorithm:
1. If `numRows` is 1 or greater than the string length, return the original string.
2. Create an array of empty strings for each row.
3. Add each character to the current row.
4. Change direction at the first and last rows.
5. Join all rows and return the result.
---------------------------------------------------------------------------------------------

# Day 7 - Reverse Integer

Problem:
Given a signed 32-bit integer `x`, return its digits reversed. If the reversed integer overflows the 32-bit signed integer range, return `0`.

Approach:
- Store the sign of the number.
- Reverse the absolute value using string slicing.
- Restore the sign.
- Return `0` if the result is outside the 32-bit signed integer range.

Algorithm:
1. Check the sign of `x`.
2. Reverse the digits of the absolute value.
3. Apply the original sign.
4. If the reversed number is outside `[-2³¹, 2³¹-1]`, return `0`.
5. Otherwise, return the reversed integer.
---------------------------------------------------------------------------------------------

# Day 8 - String to Integer

Problem:
Convert a string to a 32-bit signed integer (`atoi`) by:
- Ignoring leading spaces
- Handling `+` or `-` signs
- Reading digits until a non-digit character
- Clamping the result to the 32-bit signed integer range

 Approach:
- Remove leading whitespace.
- Determine the sign.
- Traverse the string and build the integer.
- Stop at the first non-digit character.
- Clamp the result to the range `[-2³¹, 2³¹ - 1]`.

 Algorithm:

1. Remove leading whitespaces from the string.
2. Check for an optional `+` or `-` sign.
3. Read digits one by one and form the integer.
4. Stop when a non-digit character is encountered.
5. Apply the sign to the integer.
6. Clamp the result to the 32-bit signed integer range:
   - Minimum: `-2^31`
   - Maximum: `2^31 - 1`
7. Return the final integer.
---------------------------------------------------------------------------------------------

# Day 9 - Palindrome Number

 Problem:
Given an integer `x`, return `true` if `x` is a palindrome, and `false` otherwise.

Algorithm:
1. If the number is negative, return `False`.
2. Convert the number to a string.
3. Reverse the string.
4. Compare the original string with the reversed string.
5. If both are equal, return `True`; otherwise, return `False`.
-------------------------------------------------------

# Day 10 - Regular Expression Matching

# Regular Expression Matching

## Problem Statement
Given an input string `s` and a pattern `p`, implement regular expression matching with support for:

- `.` Matches any single character.
- `*` Matches zero or more of the preceding element.

The matching should cover the entire input string.

## Algorithm
1. Create a recursive function `dp(i, j)` where:
   - `i` is the current index in the string.
   - `j` is the current index in the pattern.
2. If the pattern is completely processed, return whether the string is also fully processed.
3. Check if the current characters match.
4. If the next pattern character is `*`:
   - Skip the `character*`.
   - Or use the `*` to match one or more characters.
5. Otherwise, move to the next character in both the string and the pattern.
6. Save computed results in a memoization dictionary.
7. Return the final matching result.


