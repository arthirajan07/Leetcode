Problem Statement: 
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

 ALGORITHM:
Step 1 : Create an empty hash map (hashmap).
Step 2: Traverse the array nums using a loop.
Step 3: For each element num
     Calculate its complement:
      complement = target - num
      Check if the complement already exists in the hash map.
      If yes, return the indices of the complement and current element.
      Otherwise, store the current number and its index in the hash map.
Step 5 : Continue until the pair is found.
Step 6: Return the indices of the two numbers whose sum equals the target.