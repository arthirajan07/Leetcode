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