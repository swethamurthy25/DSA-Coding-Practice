Given an array Arr of size N, print the second largest distinct element from an array. If 2nd largest element doesn't 
exist then return -1.

Example:
Input: N = 6, Arr[] = {12, 35, 1, 10, 34, 1}
Output: 34
Explanation: The largest element of the array is 35 and the second largest element is 34.
______________________________________________________________

Solution:
1. Input is in the form of dictionary, first convert that to list
2. Then we need the distinct elements, so use the set() function of Python.
3. We need to get the second largest, so we need to sort the list by using the sort() function.
4. Now cover the edge cases, if len(list) is equal to 1, it means the list has no second elements in it, so return -1 or
5. else return the second largest element.

Time complexity is O(N)
Space complexity is O(1)

```python
def print2largest(self,arr, n):
		l1 = list(set(arr))
		l1 = sorted(l1)
		if len(l1)==1:
		    return -1
		else: return l1[-2]
```
_____________________________________________________________________________________________________________________
