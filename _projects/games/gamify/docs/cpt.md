---
layout: post
title: PYTHON AND JAVA CPT
description: PYTHON AND JAVA CPT
category: Gamify
breadcrumb: true
permalink: /cpt/concepts
---

### 1. Output
Pseudo Code
```text
studentName ← "Alice"
currentGrade ← 85

DISPLAY("Student: " + studentName)
DISPLAY("Current Grade: " + currentGrade)
```

Python
```python
studentName = "Alice"
currentGrade = 85

print("Student: " + studentName)
print("Current Grade: " + str(currentGrade)) # str: refers to string. All variable types within "print" must match, so the number grade must be converted into a string.
```
JavaScript
```javascript
let studentName = "Alice"; // creates a variable that can store a value
let currentGrade = 85; 

console.log("Student: " + studentName); // console.log: displays information in the console
console.log("CurrentGrade: " + currentGrade); // No conversion to a string is needed because JavaScript can combine the string and number with +.

```
### 2. Input
Pseudo Code
```text
studentName ← INPUT("Enter student name:")
currentGrade ← INPUT("Enter current grade:")
DISPLAY("Welcome " + studentName + "!")
DISPLAY("Current Grade: " + currentGrade)
```
Python
```python
studentName = input("Enter student name: ") # input: ask the user to enter information, the value user entered is stored in variable studentName and currentGrade. 
currentGrade = input("Enter current grade: ") # currentGrade is a string because input() returns the user’s input as a string, therefore, str() is not needed here.

print("Welcome " + studentName + "!")
print("Current Grade: " + currentGrade)

```
JavaScript
```javascript
let studentName = prompt("Enter student name:"); // prompt: asks the user to enter information
let currentGrade = prompt("Enter current grade:");

console.log("Welcome " + studentName + "!");
console.log("Current Grade: " + currentGrade);

```
### 3. List
Pseudo Code
```text
testScores ← [85, 92, 78, 90]
total ← 0

FOR EACH score IN testScores
{
  total ← total + score
}

DISPLAY("Total Points: " + total)

```
Python
```python
testScores = [85, 92, 78, 90] # []: creates a list that stores multiple values, testScores stores all of the student’s test scores.
total = 0

for score in testScores: # for: goes through each value one at a time.
    total = total + score

print("Total Points: " + str(total)) # str() converts the number total into a string, because “Total Points:” is a string and a number cannot be directly joined with a string using +.

```
JavaScript
```javascript
let testScores = [85, 92, 78, 90];
let total = 0;

for (let score of testScores) { // for...of: goes through each value in the list
    total = total + score;
}

console.log("Total Points: " + total);

```
### 4. Procedure

Pseudo Code
```text
PROCEDURE getLetterGrade(score)
{
  IF (score >= 90)
  {
    RETURN("A")
  }
  ELSE
  {
    IF (score >= 80)
    {
      RETURN("B")
    }
    ELSE
    {
      RETURN("C")
    }
  }
}

studentScore ← 88
letter ← getLetterGrade(studentScore)
DISPLAY("Grade: " + letter)
```
Python
```python
def getLetterGrade(score): # defines a function that can be used to perform a specific task
    if score >= 90: # checks if the value meet the condition
        return "A" # sends the letter grade (A, B, C) as the result if the condition is true.
    elif score >= 80: # checks another condition if the previous condition is false.
        return "B"
    else:
        return "C"


studentScore = 88
letter = getLetterGrade(studentScore)

print("Grade: " + letter)

```
JavaScript
```javascript
function getLetterGrade(score) { // function: defines a reusable block of code
    if (score >= 90) {
        return "A";
    } else if (score >= 80) {
        return "B";
    } else {
        return "C";
    }
}

let studentScore = 88;
let letter = getLetterGrade(studentScore);

console.log("Grade: " + letter);

```
### 5. Sequence
Pseudo Code
```text
testScore ← 85
homeworkScore ← 92
finalExam ← 88

testWeight ← 0.4
homeworkWeight ← 0.3
examWeight ← 0.3

finalGrade ← (testScore * testWeight) + (homeworkScore * homeworkWeight) + (finalExam * examWeight)

DISPLAY("Final Grade: " + finalGrade)
```
Python
```python
testScore = 85
homeworkScore = 92
finalExam = 88

testWeight = 0.4
homeworkWeight = 0.3
examWeight = 0.3

finalGrade = (testScore * testWeight) + (homeworkScore * homeworkWeight) + (finalExam * examWeight)

print("Final Grade: " + str(finalGrade))

```
JavaScript
```javascript
let testScore = 85;
let homeworkScore = 92;
let finalExam = 88;

let testWeight = 0.4;
let homeworkWeight = 0.3;
let examWeight = 0.3;

let finalGrade = (testScore * testWeight) + (homeworkScore * homeworkWeight) + (finalExam * examWeight);

console.log("Final Grade: " + finalGrade);
```
### 6. Selection
Pseudo Code
```text
score ← INPUT("Grade: 0 - 100")
grade ← "Unknown"

IF (score >= 90)
{
  grade ← "A"
}
ELSE
{
  IF (score >= 80)
  {
    grade ← "B"
  }
  ELSE
  {
    IF (score >= 70)
    {
      grade ← "C"
    }
    ELSE
    {
      IF (score >= 60)
      {
        grade ← "D"
      }
      ELSE
      {
        grade ← "F"
      }
    }
  }
}

DISPLAY("Your grade is: " + grade)
```
Python
```python
score = input("Grade: 0 - 100")
grade = "Unknown"

if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 70:
    grade = "C"
elif score >= 60:
    grade = "D"
else:
    grade = "F"

print("Your grade is: " + grade)

```
JavaScript
```javascript
score = (input("Grade: 0 - 100")
grade = "Unknown"

if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 70:
    grade = "C"
elif score >= 60:
    grade = "D"
else:
    grade = "F"

print("Your grade is: " + grade)
```
### 7. Iteration
Pseudo Code
```text
DISPLAY("Grade Entry System")

grades ← [] 
gradeCount ← 0
totalPoints ← 0
continueEntry ← "yes"

REPEAT UNTIL (continueEntry = "no")
{
  grade ← INPUT("Add a grade:")
  
  APPEND(grades, grade)
  gradeCount ← gradeCount + 1
  totalPoints ← totalPoints + grade
  
  continueEntry ← INPUT("Continue entering grades? (no to stop)")
}

DISPLAY("List of grades: " + grades)
DISPLAY("Total grades entered: " + gradeCount)
DISPLAY("Total points: " + totalPoints)

```
Python
```python
print("Grade Entry System")

grades = []
gradeCount = 0
totalPoints = 0
continueEntry = "yes"

while continueEntry != "no": # while: repeats the code as long as the condition is true; !: not equal to.
    grade = float(input("Add a grade: ")) # float: converts the input into a number that can include decimals.

    grades.append(grade) # append: adds the new grade to the end of the grades list. 
    gradeCount = gradeCount + 1
    totalPoints = totalPoints + grade

    continueEntry = input("Continue entering grades? (no to stop): ")

print("List of grades:", grades)
print("Total grades entered:", gradeCount)
print("Total points:", totalPoints)

```
JavaScript
```javascript
console.log("Grade Entry System");

let grades = [];
let gradeCount = 0;
let totalPoints = 0;
let continueEntry = "yes";

while (continueEntry !== "no") {
    let grade = Number(prompt("Add a grade:"));  // Number: converts the input from a string into a number

    grades.push(grade); //// push: adds the grade to the end of the list
    gradeCount = gradeCount + 1;
    totalPoints = totalPoints + grade;

    continueEntry = prompt("Continue entering grades? (no to stop)");
}

console.log("List of grades: " + grades);
console.log("Total grades entered: " + gradeCount);
console.log("Total points: " + totalPoints);
```
### 8. Algorithm
Pseudo Code
```text
PROCEDURE calculateAverage(numbers)
{
  total ← 0
  count ← 0
  
  FOR EACH num IN numbers
  {
    total ← total + num
    count ← count + 1
  }
  
  IF (count > 0)
  {
    average ← total / count # # calculates the average by dividing the total by the number of values
    RETURN(average)
  }
  ELSE
  {
    RETURN(0)
  }
}

scores ← [85, 92, 78, 95, 88]
result ← calculateAverage(scores)
DISPLAY("Average score: " + result)

DISPLAY{"Scores: " + scores}
IF (result >= 90)
{
  DISPLAY("Grade: A")
}
ELSE
{
  DISPLAY("Grade: B or lower")
}

```
Python
```python
def calculateAverage(numbers):
    total = 0
    count = 0

    for num in numbers:
        total = total + num # num: the current number.
        count = count + 1

    if count > 0:
        average = total / count
        return average
    else:
        return 0 # else return 0 to avoid dividing by zero.


scores = [85, 92, 78, 95, 88]
result = calculateAverage(scores)

print("Average score: " + str(result))
print("Scores: " + str(scores))

if result >= 90:
    print("Grade: A")
else:
    print("Grade: B or lower")

```
JavaScript
```javascript
function calculateAverage(numbers) {
    let total = 0;
    let count = 0;

    for (let num of numbers) {
        total = total + num;
        count = count + 1;
    }

    if (count > 0) {
        let average = total / count;
        return average;
    } else {
        return 0;
    }
}

let scores = [85, 92, 78, 95, 88];
let result = calculateAverage(scores);

console.log("Average score: " + result);
console.log("Scores: " + scores);

if (result >= 90) {
    console.log("Grade: A");
} else {
    console.log("Grade: B or lower");
}
```
### 9. List Operations
Pseudo Code
```text
PROCEDURE findItem(items, target)
{
  index ← 1
  
  FOR EACH item IN items
  {
    IF (item = target)
    {
      RETURN(index)
    }
    index ← index + 1
  }
  
  RETURN(-1)
}

students ← ["Alice", "Bob", "Carol", "Dave"]
searchFor ← INPUT("Enter student you are looking for...")

position ← findItem(students, searchFor)

IF (position > 0)
{
  DISPLAY("Found at position: " + position)
}
ELSE
{
  DISPLAY("Not found")
}
```
Python
```python
def findItem(items, target):
    index = 1

    for item in items:
        if item == target:
            return index
        index = index + 1

    return -1


students = ["Alice", "Bob", "Carol", "Dave"]
searchFor = input("Enter student you are looking for...")

position = findItem(students, searchFor)

if position > 0:
    print("Found at position: " + str(position))
else:
    print("Not found")

```
JavaScript
```javascript
function findItem(items, target) {
    let index = 1;

    for (let item of items) {
        if (item === target) {
            return index;
        }
        index = index + 1;
    }

    return -1;
}

let students = ["Alice", "Bob", "Carol", "Dave"];
let searchFor = prompt("Enter student you are looking for...");

let position = findItem(students, searchFor);

if (position > 0) {
    console.log("Found at position: " + position);
} else {
    console.log("Not found");
}
```
### 10. List Operations
Pseudo Code
```text
tasks ← ["homework", "project"]
DISPLAY("Initial:" + tasks)

APPEND(tasks, "study")
DISPLAY("After APPEND:" + tasks)

INSERT(tasks, 2, "practice")
DISPLAY("After INSERT at 2:" + tasks)

REMOVE(tasks, 3)
DISPLAY("After REMOVE at 3: " + tasks)

length ← LENGTH(tasks)
DISPLAY("List length: " + length)

FOR EACH task IN tasks
{
  DISPLAY("Task: " + task)
}
```
Python
```python
tasks = ["homework", "project"]
print("Initial: " + str(tasks))

tasks.append("study")
print("After APPEND: " + str(tasks))

tasks.insert(1, "practice")
print("After INSERT at 2: " + str(tasks))

tasks.pop(2)
print("After REMOVE at 3: " + str(tasks))

length = len(tasks)
print("List length: " + str(length))

for task in tasks:
    print("Task: " + task)

```
JavaScript
```javascript
let tasks = ["homework", "project"];
console.log("Initial: " + tasks);

tasks.push("study"); // push: adds an item to the end of the list
console.log("After APPEND: " + tasks);

tasks.splice(1, 0, "practice"); // splice: inserts "practice" at index 1
console.log("After INSERT at 2: " + tasks);

tasks.splice(2, 1); // splice: removes 1 item starting at index 2
console.log("After REMOVE at 3: " + tasks);

let length = tasks.length; // length: gives the number of items in the list
console.log("List length: " + length);

for (let task of tasks) {
    console.log("Task: " + task);
}
```
### 11. Search Algorithm
Pseudo Code
```text
PROCEDURE findStudent(studentList, targetName)
{
  index ← 1
  
  FOR EACH student IN studentList
  {
    IF (student = targetName)
    {
      RETURN(index)
    }
    index ← index + 1
  }
  
  RETURN(-1)
}

students ← ["Alice", "Bob", "Carol", "Dave"]
grades ← [92, 85, 88, 76]

searchName ← INPUT("Enter student name to search:")

position ← findStudent(students, searchName)

IF (position > 0)
{
  studentGrade ← grades[position]
  DISPLAY("Student found at position: " + position)
  DISPLAY("Grade: " + studentGrade)
}
ELSE
{
  DISPLAY("Student not found in roster")
}
```
Python
```python
def findStudent(studentList, targetName):
    index = 1

    for student in studentList:
        if student == targetName:
            return index
        index = index + 1

    return -1


students = ["Alice", "Bob", "Carol", "Dave"]
grades = [92, 85, 88, 76]

searchName = input("Enter student name to search: ")

position = findStudent(students, searchName)

if position > 0:
    studentGrade = grades[position - 1] # subtracts 1 because the search position starts at 1, while Python list indexes start at 0
    print("Student found at position: " + str(position))
    print("Grade: " + str(studentGrade))
else:
    print("Student not found in roster")
```
JavaScript
```javascript
function findStudent(studentList, targetName) {
    let index = 1;

    for (let student of studentList) {
        if (student === targetName) {
            return index;
        }
        index = index + 1;
    }

    return -1;
}

let students = ["Alice", "Bob", "Carol", "Dave"];
let grades = [92, 85, 88, 76];

let searchName = prompt("Enter student name to search:");

let position = findStudent(students, searchName);

if (position > 0) {
    let studentGrade = grades[position - 1];
    console.log("Student found at position: " + position);
    console.log("Grade: " + studentGrade);
} else {
    console.log("Student not found in roster");
}

```
### 12. Boolean Logic
Pseudo Code
```text
PROCEDURE findStudentGrade(students, scores, targetName)
{
  index ← 1
  
  FOR EACH student IN students
  {
    IF (student = targetName)
    {
      grade ← scores[index]
      RETURN(grade)
    }
    index ← index + 1
  }
  
  RETURN(-1)
}

students ← ["Alice", "Bob", "Carol", "Dave"]
scores ← [92, 85, 88, 76]

searchName ← INPUT("Enter student name:")

result ← findStudentGrade(students, scores, searchName)

IF (result > 0)
{
  DISPLAY("Grade for " + searchName + ": " + result)
}
ELSE
{
  DISPLAY("Student not found")
}
```
Python
```python
def findStudentGrade(students, scores, targetName):
    index = 1

    for student in students:
        if student == targetName:
            grade = scores[index - 1]
            return grade
        index = index + 1

    return -1


students = ["Alice", "Bob", "Carol", "Dave"]
scores = [92, 85, 88, 76]

searchName = input("Enter student name: ")

result = findStudentGrade(students, scores, searchName)

if result > 0:
    print("Grade for " + searchName + ": " + str(result))
else:
    print("Student not found")
```
JavaScript
```javascript
function findStudentGrade(students, scores, targetName) {
    let index = 1;

    for (let student of students) {
        if (student === targetName) { // ===: checks whether the values are equal
            let grade = scores[index - 1];
            return grade;
        }
        index = index + 1;
    }

    return -1;
}

let students = ["Alice", "Bob", "Carol", "Dave"];
let scores = [92, 85, 88, 76];

let searchName = prompt("Enter student name:");

let result = findStudentGrade(students, scores, searchName);

if (result > 0) {
    console.log("Grade for " + searchName + ": " + result);
} else {
    console.log("Student not found");


```
