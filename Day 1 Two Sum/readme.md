PROBLEM STATEMENT:
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.
You may assume that each input would have exactly one solution, and you may not use the same element twice.

DESCRIPTION:
The twoSum function finds the indices of two numbers in the given array nums whose sum is equal to the given target.
It uses a brute-force approach by checking every possible pair of elements in the array. If a pair whose sum equals the target is found, the function immediately returns their indices. If no such pair exists, it returns an empty vector.

ALGORITHM:
STEP 1: Start from the first element of the array.
STEP 2: Compare it with every element that comes after it.
STEP 3: Add the two elements.
STEP 4: If their sum is equal to the target, return their indices.
STEP 5: If not, continue checking the next pair.
STEP 6: Repeat this process until a matching pair is found.
STEP 7: If no pair is found after checking all possible pairs, return an empty vector {}.