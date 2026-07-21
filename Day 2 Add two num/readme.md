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

