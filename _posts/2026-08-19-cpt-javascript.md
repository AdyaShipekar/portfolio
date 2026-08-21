---
layout: post
title: JavaScript CPT
description: JAVASCRIPT CPT
breadcrumb: true
codemirror: true
permalink: /cpt/concepts/javascript
---

### 1. Output
Pseudo Code
```text
studentName ← "Alice"
currentGrade ← 85

DISPLAY("Student: " + studentName)
DISPLAY("Current Grade: " + currentGrade)
```

JavaScript
{% capture js_output_code %}
let studentName = "Alice"; // creates a variable that can store a value
let currentGrade = 85;

console.log("Student: " + studentName); // console.log: displays information in the console
console.log("CurrentGrade: " + currentGrade); // No conversion to a string is needed because JavaScript can combine the string and number with +.
{% endcapture %}

{% include runners/code.html
  runner_id="js-output"
  language="javascript"
  variants_key="output"
  code=js_output_code
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

JavaScript
{% capture js_input_code %}
let studentName = prompt("Enter student name:"); // prompt: asks the user to enter information
let currentGrade = prompt("Enter current grade:");

console.log("Welcome " + studentName + "!");
console.log("Current Grade: " + currentGrade);
{% endcapture %}

{% include runners/code.html
  runner_id="js-input"
  language="javascript"
  variants_key="input"
  code=js_input_code
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

JavaScript
{% capture js_list_code %}
let testScores = [85, 92, 78, 90];
let total = 0;

for (let score of testScores) { // for...of: goes through each value in the list
    total = total + score;
}

console.log("Total Points: " + total);
{% endcapture %}

{% include runners/code.html
  runner_id="js-list"
  language="javascript"
  variants_key="list"
  code=js_list_code
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

JavaScript
{% capture js_procedure_code %}
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
{% endcapture %}

{% include runners/code.html
  runner_id="js-procedure"
  language="javascript"
  variants_key="procedure"
  code=js_procedure_code
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

JavaScript
{% capture js_sequence_code %}
let testScore = 85;
let homeworkScore = 92;
let finalExam = 88;

let testWeight = 0.4;
let homeworkWeight = 0.3;
let examWeight = 0.3;

let finalGrade = (testScore * testWeight) + (homeworkScore * homeworkWeight) + (finalExam * examWeight);

console.log("Final Grade: " + finalGrade);
{% endcapture %}

{% include runners/code.html
  runner_id="js-sequence"
  language="javascript"
  variants_key="sequence"
  code=js_sequence_code
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

JavaScript
{% capture js_selection_code %}
const score = Number(prompt("Grade: 0 - 100"));
let grade = "Unknown";

if (score >= 90) {
  grade = "A";
} else if (score >= 80) {
  grade = "B";
} else if (score >= 70) {
  grade = "C";
} else if (score >= 60) {
  grade = "D";
} else {
  grade = "F";
}

console.log("Your grade is: " + grade);
{% endcapture %}

{% include runners/code.html
  runner_id="js-selection"
  language="javascript"
  variants_key="selection"
  code=js_selection_code
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

JavaScript
{% capture js_iteration_code %}
console.log("Grade Entry System");

let grades = [];
let gradeCount = 0;
let totalPoints = 0;
let continueEntry = "yes";

while (continueEntry !== "no") {
    let grade = Number(prompt("Add a grade:"));  // Number: converts the input from a string into a number

    grades.push(grade); // push: adds the grade to the end of the list
    gradeCount = gradeCount + 1;
    totalPoints = totalPoints + grade;

    continueEntry = prompt("Continue entering grades? (no to stop)");
}

console.log("List of grades: " + grades);
console.log("Total grades entered: " + gradeCount);
console.log("Total points: " + totalPoints);
{% endcapture %}

{% include runners/code.html
  runner_id="js-iteration"
  language="javascript"
  variants_key="iteration"
  code=js_iteration_code
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

JavaScript
{% capture js_algorithm_code %}
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
{% endcapture %}

{% include runners/code.html
  runner_id="js-algorithm"
  language="javascript"
  variants_key="algorithm"
  code=js_algorithm_code
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

JavaScript
{% capture js_list_ops_1_code %}
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
{% endcapture %}

{% include runners/code.html
  runner_id="js-list-ops-1"
  language="javascript"
  variants_key="list-ops-1"
  code=js_list_ops_1_code
  height="340px"
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

JavaScript
{% capture js_list_ops_2_code %}
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
{% endcapture %}

{% include runners/code.html
  runner_id="js-list-ops-2"
  language="javascript"
  variants_key="list-ops-2"
  code=js_list_ops_2_code
  height="340px"
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

JavaScript
{% capture js_search_code %}
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
{% endcapture %}

{% include runners/code.html
  runner_id="js-search"
  language="javascript"
  variants_key="search"
  code=js_search_code
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

JavaScript
{% capture js_boolean_code %}
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
}
{% endcapture %}

{% include runners/code.html
  runner_id="js-boolean"
  language="javascript"
  variants_key="boolean"
  code=js_boolean_code
  height="360px"
%}

<script>
(function () {
  function patchJsRunners() {
    document.querySelectorAll('.code-runner-container').forEach(function (container) {
      var sel = container.querySelector('.languageSelect');
      if (!sel || sel.value !== 'javascript') return;
      var btn = container.querySelector('.runBtn');
      if (!btn) return;
      var newBtn = btn.cloneNode(true);
      btn.parentNode.replaceChild(newBtn, btn);
      newBtn.addEventListener('click', function () {
        var cm = container.querySelector('.CodeMirror') && container.querySelector('.CodeMirror').CodeMirror;
        if (!cm) return;
        var code = cm.getValue();
        var outEl = container.querySelector('.output-content');
        var etEl  = container.querySelector('.execTime');
        outEl.textContent = '⏳ Running…';
        if (etEl) etEl.textContent = '';
        var t0 = Date.now(), logs = [], origLog = console.log;
        console.log = function () { logs.push(Array.from(arguments).map(String).join(' ')); origLog.apply(console, arguments); };
        try {
          eval(code);
          console.log = origLog;
          outEl.textContent = logs.length ? logs.join('\n') : '[no output]';
          if (etEl) etEl.textContent = '⏱ Execution time: ' + (Date.now() - t0) + 'ms';
        } catch (e) {
          console.log = origLog;
          outEl.textContent = 'Error: ' + e.message;
          if (etEl) etEl.textContent = '';
        }
      });
    });
  }
  document.addEventListener('DOMContentLoaded', patchJsRunners);
})();
</script>
