---
layout: post
title: Python CPT
description: PYTHON CPT
breadcrumb: true
codemirror: true
permalink: /cpt/concepts/python
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
{% capture py_output_code %}
studentName = "Alice"
currentGrade = 85

print("Student: " + studentName)
print("Current Grade: " + str(currentGrade)) # str: refers to string. All variable types within "print" must match, so the number grade must be converted into a string.
{% endcapture %}

{% include runners/code.html
  runner_id="py-output"
  language="python"
  variants_key="output"
  local_python=true
  code=py_output_code
  height="200px"
%}

### 2. Input
Pseudo Code
```text
studentName ← INPUT("Enter student name:")
currentGrade ← INPUT("Enter current grade:")
DISPLAY("Welcome " + studentName + "!")
DISPLAY("Current Grade: " + currentGrade)
```

Python
{% capture py_input_code %}
studentName = input("Enter student name: ") # input: ask the user to enter information, the value user entered is stored in variable studentName and currentGrade.
currentGrade = input("Enter current grade: ") # currentGrade is a string because input() returns the user's input as a string, therefore, str() is not needed here.

print("Welcome " + studentName + "!")
print("Current Grade: " + currentGrade)
{% endcapture %}

{% include runners/code.html
  runner_id="py-input"
  language="python"
  variants_key="input"
  local_python=true
  code=py_input_code
  height="200px"
%}

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
{% capture py_list_code %}
testScores = [85, 92, 78, 90] # []: creates a list that stores multiple values, testScores stores all of the student's test scores.
total = 0

for score in testScores: # for: goes through each value one at a time.
    total = total + score

print("Total Points: " + str(total)) # str() converts the number total into a string, because "Total Points:" is a string and a number cannot be directly joined with a string using +.
{% endcapture %}

{% include runners/code.html
  runner_id="py-list"
  language="python"
  variants_key="list"
  local_python=true
  code=py_list_code
  height="220px"
%}

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
{% capture py_procedure_code %}
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
{% endcapture %}

{% include runners/code.html
  runner_id="py-procedure"
  language="python"
  variants_key="procedure"
  local_python=true
  code=py_procedure_code
  height="300px"
%}

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
{% capture py_sequence_code %}
testScore = 85
homeworkScore = 92
finalExam = 88

testWeight = 0.4
homeworkWeight = 0.3
examWeight = 0.3

finalGrade = (testScore * testWeight) + (homeworkScore * homeworkWeight) + (finalExam * examWeight)

print("Final Grade: " + str(finalGrade))
{% endcapture %}

{% include runners/code.html
  runner_id="py-sequence"
  language="python"
  variants_key="sequence"
  local_python=true
  code=py_sequence_code
  height="280px"
%}

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
{% capture py_selection_code %}
score = int(input("Grade: 0 - 100"))
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
{% endcapture %}

{% include runners/code.html
  runner_id="py-selection"
  language="python"
  variants_key="selection"
  local_python=true
  code=py_selection_code
  height="320px"
%}

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
{% capture py_iteration_code %}
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
{% endcapture %}

{% include runners/code.html
  runner_id="py-iteration"
  language="python"
  variants_key="iteration"
  local_python=true
  code=py_iteration_code
  height="400px"
%}

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
    average ← total / count
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
{% capture py_algorithm_code %}
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
{% endcapture %}

{% include runners/code.html
  runner_id="py-algorithm"
  language="python"
  variants_key="algorithm"
  local_python=true
  code=py_algorithm_code
  height="450px"
%}

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
{% capture py_list_ops_1_code %}
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
{% endcapture %}

{% include runners/code.html
  runner_id="py-list-ops-1"
  language="python"
  variants_key="list-ops-1"
  local_python=true
  code=py_list_ops_1_code
  height="320px"
%}

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
{% capture py_list_ops_2_code %}
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
{% endcapture %}

{% include runners/code.html
  runner_id="py-list-ops-2"
  language="python"
  variants_key="list-ops-2"
  local_python=true
  code=py_list_ops_2_code
  height="320px"
%}

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
{% capture py_search_code %}
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
{% endcapture %}

{% include runners/code.html
  runner_id="py-search"
  language="python"
  variants_key="search"
  local_python=true
  code=py_search_code
  height="360px"
%}

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
{% capture py_boolean_code %}
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
{% endcapture %}

{% include runners/code.html
  runner_id="py-boolean"
  language="python"
  variants_key="boolean"
  local_python=true
  code=py_boolean_code
  height="360px"
%}

<script>
(function () {
  var _pyReady = null;

  function getPyodide() {
    if (!_pyReady) {
      _pyReady = new Promise(function (resolve, reject) {
        var s = document.createElement('script');
        s.src = 'https://cdn.jsdelivr.net/pyodide/v0.27.0/full/pyodide.js';
        s.onload = function () {
          loadPyodide().then(function (py) {
            py.runPython(
              'import builtins\n' +
              'from js import prompt as _prompt\n' +
              'def _input(question=""):\n' +
              '    r = _prompt(question)\n' +
              '    return "" if r is None else r\n' +
              'builtins.input = _input'
            );
            resolve(py);
          }).catch(reject);
        };
        s.onerror = reject;
        document.head.appendChild(s);
      });
    }
    return _pyReady;
  }

  function patchPyRunners() {
    document.querySelectorAll('.code-runner-container').forEach(function (container) {
      var sel = container.querySelector('.languageSelect');
      if (!sel || sel.value !== 'python') return;
      var btn = container.querySelector('.runBtn');
      if (!btn) return;
      var newBtn = btn.cloneNode(true);
      btn.parentNode.replaceChild(newBtn, btn);
      newBtn.addEventListener('click', async function () {
        var cm = container.querySelector('.CodeMirror') && container.querySelector('.CodeMirror').CodeMirror;
        if (!cm) return;
        var code = cm.getValue();
        var outEl = container.querySelector('.output-content');
        var etEl  = container.querySelector('.execTime');
        outEl.textContent = '⏳ Loading Python runtime…';
        if (etEl) etEl.textContent = '';
        var t0 = Date.now();
        try {
          var py = await getPyodide();
          var lines = [];
          py.setStdout({ batched: function (s) { lines.push(s); } });
          outEl.textContent = '⏳ Running…';
          await py.runPythonAsync(code);
          outEl.textContent = lines.join('\n') || '[no output]';
          if (etEl) etEl.textContent = '⏱ Execution time: ' + (Date.now() - t0) + 'ms';
        } catch (e) {
          outEl.textContent = 'Error: ' + e.message;
          if (etEl) etEl.textContent = '';
        }
      });
    });
  }

  document.addEventListener('DOMContentLoaded', patchPyRunners);
})();
</script>
