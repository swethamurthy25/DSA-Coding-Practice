Given two arrays A and B of equal size N, the task is to find if the given arrays are equal or not. 
Two arrays are said to be equal if both of them contain the same set of elements, arrangements (or permutations) of 
elements may be different though.

Note: If there are repetitions, then counts of repeated elements must also be the same for two arrays to be equal.

Complete check() function which takes both the given array and their size as function arguments and returns true if the arrays are equal else returns false.
The 0 and 1 printing is done by the driver code.

Example 1:

Input:N = 5

A[] = {1,2,5,4,0} and B[] = {2,4,5,0,1}

Output: 1

Explanation: Both the array can be rearranged to {0,1,2,4,5}

Example 2:

Input:N = 3

A[] = {1,2,5} and B[] = {2,4,15}

Output: 0

Explanation: A[] and B[] have only one common value.
____________________________________________________________________________________

```python
class Solution:
    #Function to check if two arrays are equal or not.
    def check(self,A,B,N):
        if len(A) != len(B):return 0
        A = sorted(A)
        B = sorted(B)
        if A == B:
            return 1
        else: return 0
```
____________________________________________________________________________________________
