Given the names and grades for each student in a class of N students, store them in a nested list and print the name(s) 
of any student(s) having the second lowest grade.

Note: 

If there are multiple students with the second lowest grade, order their names alphabetically and print each name on a 
new line.

INPUT FORMAT:
* The first line contains an N integer, the number of students.
* The 2N subsequent lines describe each student over  lines.
* The first line contains a student's name.
* The second line contains their grade.

CONSTRAINTS:
2 <= N <= 5
There will always be one or more students having the second lowest grade.

OUTPUT FORMAT:
* Print the name(s) of any student(s) having the second lowest grade. 
* If there are multiple students, order their names alphabetically and print each one on a new line.

SAMPLE INPUT:
5
Harry
37.21
Berry
37.21
Tina
37.2
Akriti
41
Harsh
39

SAMPLE OUTPUT:
Berry
Harry

EXPLANATION:
* There are  students in this class whose names and grades are assembled to build the following list:
* students = [['Harry', 37.21], ['Berry', 37.21], ['Tina', 37.2], ['Akriti', 41], ['Harsh', 39]]
* The lowest grade of 37.2 belongs to Tina. The second lowest grade of 37.21 belongs to both Harry and Berry,
  so we order their names alphabetically and 
* print each name on a new line.
____________________________________________________________________________________________________________________

UNDERSTANDING THE GIVEN DETAILS:

- We are provided with names as strings and scores as float values, but they are not in a nested list.
- We are given with N value and the N number of inputs (with names and score)
- We have to form the input in a nested list before solving the question.
- Use for loop to get inputs - names and score from the user and append it to a nested list

```python
n = int(input())
nested_list=[]
for i in range():
  name = input()
  score = float(input())
  nested_list.append([name,score])
    
- Now we got the input list , we need to find the second lowest grade.
- Now iterate through the nested_list and get only the grades and append it to another new list , but iterating again will increase the time complexity.
- As an alternative , while appending the nested_list , append the grade list also simultaneously

n = int(input())
nested_list=[]
grade=[]
for i in range():
  name = input()
  score = float(input())
  nested_list.append([name,score])
  grade.append(score)
```

- Now there are two ways to get the second lowest grade.
- Approach 1: Sort the grade list and compare the first minimum value with rest of the value in list to get the second lowest
- Approach 2: Using the set function to remove the duplicates and then sort the list. After sorting , we can get second lowest by retrieving the x[1] element.
- Here we are using approach 2 to find the second lowest grade.

n = int(input())
nested_list=[]
grade=[]
for i in range():
  name = input()
  score = float(input())
  nested_list.append([name,score])
  grade.append(score)
grade=sorted(set(grade))
second_lowest=grade[1]

- Now we have to compare the second lowest mark to the nested_list and get only the names that matches the score and append the names to new list
- Use for loop to iterate over nested list and get the names that matches the score
- Sort the names to get it in alphabatical order and print it

n = int(input())
nested_list=[]
grade=[]
for i in range():
  name = input()
  score = float(input())
  nested_list.append([name,score])
  grade.append(score)
grade=sorted(set(grade))
second_lowest=grade[1]
name=[]
for val in nested_list:
  if second_lowest=val[1]:
    name.append(val[0])
name.sort()
for nm in name:
  print(nm)
  
____________________________________________________________________________________________________________________________





