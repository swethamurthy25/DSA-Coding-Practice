You are given an array arr of n integers. 
You must return the minimum number of operations required to make this array 0. 

For this you can do an operation :
Choose a sub-array of non-zero elements & replace all with 0(0 must be present in arr, if not you can not replace it).

Example 1:
Input: n = 4, arr = {3,0,4,5} and Output:2

Explanation:
First, we can choose 3 replace with 0(which is on 1st Index) and in the second operation, we can choose 4 & 5 -> replace with 0(1st Index).

Example 2:
Input: n = 8 , arr = {10,4,9,6,10,10,4,4} and Output: -1 

Explanation: 
If we do operations here, we can not make the entire 0 
because no 0 is present in the array, hence -1.

Your Task:
* You don't need to read input or print anything.
* Your task is to complete the function arrayOperations() which takes an integer n, and an array arr as inputs, and find the 
minimum number of operations you must perform to make all the elements of the array 0.
* If not possible return -1;

Expected Time Complexity: O(N)

Expected Auxiliary Space: O(1)

Constraints:
1 <= n <= 105
0 <= arr[i] <= 109
________________________________________________________________________________________________________________

Understanding:
- Look for edge case, if the array does not contain 0 , we cannot perform any operation ,so directly return -1
- If the arr contain 0 , the nonzero elements can be replaced and the number of operations can be calculated and returned as result.

Solution:
1. The code begins with an edge case check to ensure that there is at least one 0 in the array. If there is no 0 in the array, the method immediately returns -1, 
   since it is not possible to perform the required operation on the array.
2. Next, the code initializes two variables i and j. The i variable is used to keep track of the number of operations performed, and the j variable is used to track 
   the position of the zero elements in the array.
```python
class Solution:
    def arrayOperations(self, n : int, arr : List[int]) -> int:
        #Edge case
        if 0 not in arr:return -1
        i = 0
        j = 0   
 ```       
3. Use while loop for iteration and check if the j value is less than the len(arr), and if the element is equal to 0 , then in that case increment the j count by 1
while j < len(arr):
            if arr[j] == 0:
                j += 1
4. Else ,If the current element is non-zero, the loop increments i value by 1 and then enters another while loop that advances the index j to the next zero element in 
   the array.
5. Return the non-zero element value i as a final result.

Code:
```python
class Solution:
    def arrayOperations(self, n : int, arr : List[int]) -> int:
        #Edge case
        if 0 not in arr: return -1

        i = 0
        j = 0        
        while j < len(arr):
            if arr[j] == 0:
                j += 1
            else:
                i += 1
                while j < len(arr) and arr[j] != 0:
                    j += 1
        return I
```
 ______________________________________________________________________________________________________________















