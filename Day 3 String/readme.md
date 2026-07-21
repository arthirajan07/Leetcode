# Longest Substring Without Repeating Characters

## Problem Statement
Given a string `s`, find the length of the longest substring without repeating characters.

## Approach
Used the Sliding Window technique with a Hash Set to maintain unique characters within the current window. If a duplicate character is found, the left pointer moves forward until the duplicate is removed.

## Algorithm
1. Initialize an empty set.
2. Use two pointers (`left` and `right`) to represent the sliding window.
3. Expand the window by moving `right`.
4. If a duplicate character is found, shrink the window from the left.
5. Update the maximum length found.
6. Return the maximum length.

## Time Complexity
O(n)

## Space Complexity
O(min(n, m))