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
