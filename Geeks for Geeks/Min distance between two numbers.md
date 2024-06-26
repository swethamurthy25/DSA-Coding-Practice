
You are given an array A, of N elements. Find the minimum index-based distance between two elements of the array, x, 
and y such that (x!=y)

Input:

N = 4 and A[] = {1,2,3,2} and x = 1, y = 2

Output: 1

Explanation: x = 1 and y = 2. There are two distances between x and y, which are 1 and 3 out of which the least is 1.

Input:
N = 7
A[] = {86,39,90,67,84,66,62}
x = 42, y = 12
Output: -1
Explanation: x = 42 and y = 12. We return
-1 as x and y don't exist in the array.

Your Task:

Complete the function minDist() which takes the array, n, x, and y as input parameters and returns the minimum 
distance between x and y in the array. If no such distance is possible then return -1.

Expected Time Complexity: O(N)
Expected Auxiliary Space: O(1)

Constraints:
1 <= N <= 105
0 <= A[i], x, y <= 105
_________________________________________________________________________________________________________________

Things to note down: 
The given array also contains duplicate numbers/repeated numbers, so we may get many different distances.

Approach:

1. We are given with size of the array, the array elements, and x and y values.
2. First check whether the x and y values exist in the array. If it does not exist, directly return -1.
3. If exists, check for the distance between those two elements.
4. If multiple combinations exist, we will get 2 or 3 distances, and return the least value among that as a result.

