Mr. Vincent works in a door mat manufacturing company. One day, he designed a new doormat with the following specifications:
* Mat size must be N X M . (N is an odd natural number, and M is 3 times N.)
* The design should have 'WELCOME' written in the center.
* The design pattern should only use |, . and - characters.

Input Format
A single line containing the space-separated values of N and M.

Output Format
Output the design pattern.

Sample Input:
9 27

Output:
```python
------------.|.------------
---------.|..|..|.---------
------.|..|..|..|..|.------
---.|..|..|..|..|..|..|.---
----------WELCOME----------
---.|..|..|..|..|..|..|.---
------.|..|..|..|..|.------
---------.|..|..|.---------
------------.|.------------
```
___________________________________________________________________________________________________________________

Solution:

1. First we need to get N and M values as input from the user, separated by space. 
N,M = input().split()

2. But the input will be in string format. We need to have the values in integer format. So, we need to use the map function in python.
N,M = map(int, input().split())

3. The most trickiest part here is to understand at which point the center lies and how the formation of the patterns happens. We can use the center function of the python
   here. 
   For example: ('.|.').center(21)
   This code will fix the icon in the center by equally dividing the 21 spaces.
   
   '         .|.         '
   
4. So we need to get this icon printed in a pattern say - 1st line has one icon, 2nd has 3, and 3rd line has 5.
5. SO we need to use the for loop for this.
   
```python
for i in range(1,N,2):
    print(('.|.' * i).center(M,'-'))
    
 ---------.|.---------
------.|..|..|.------
---.|..|..|..|..|.---
.|..|..|..|..|..|..|.
```

5. Same way we need to form the bottom part using the for-loop

```python
for i in range(N-2,-1,-2):
    print(('.|.' * i).center(M,'-'))
    
.|..|..|..|..|..|..|.
---.|..|..|..|..|.---
------.|..|..|.------
---------.|.---------
```

6. Now will include the print statement in the middle and combine both the codes.

```python
N,M = map(int,input().split())
for i in range(1,N,2):
    print(('.|.' * i).center(M,'-'))
    
print('WELCOME'.center(M,'-'))

for i in range(N-2,-1,-2):
    print(('.|.' * i).center(M,'-'))
    
---------.|.---------
------.|..|..|.------
---.|..|..|..|..|.---
.|..|..|..|..|..|..|.
-------WELCOME-------
.|..|..|..|..|..|..|.
---.|..|..|..|..|.---
------.|..|..|.------
---------.|.---------
```
_____________________________________________________________________________________________________________________


