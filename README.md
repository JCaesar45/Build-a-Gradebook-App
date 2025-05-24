```
# Gradebook App

## Overview

This Gradebook App provides basic functionality to calculate student grades, class averages, and pass/fail status based on test scores.

The app includes four main functions:

* **getAverage(scores):** Calculates the average score from an array of test scores.
* **getGrade(score):** Converts a numeric score to a letter grade based on predefined ranges.
* **hasPassingGrade(score):** Determines if a score corresponds to a passing grade using the letter grade.
* **studentMsg(scores, studentScore):** Generates a message summarizing the class average, the student's grade, and their pass/fail status.

## Functionality

### getAverage(scores)

* **Input:** Array of test scores (numbers).
* **Output:** Average score (number).
* Returns `0` if the input array is empty.

### getGrade(score)

* **Input:** Student score (number).
* **Output:** Letter grade (string).
* **Grading Scale:**

| Score Range | Grade |
| ----------- | ----- |
| 100         | "A+"  |
| 90 - 99     | "A"   |
| 80 - 89     | "B"   |
| 70 - 79     | "C"   |
| 60 - 69     | "D"   |
| 0 - 59      | "F"   |

### hasPassingGrade(score)

* **Input:** Student score (number).
* **Output:** Boolean (`true` if passing, `false` if failing).
* Uses `getGrade` internally.
* Passing grade is any letter grade other than "F".

### studentMsg(scores, studentScore)

* **Input:**

  * `scores`: Array of all test scores (numbers).
  * `studentScore`: Individual student score (number).
* **Output:** String message summarizing:

  * Class average
  * Student letter grade
  * Pass/fail status

**Example output:**

``
Class average: 85. Your grade: B. You passed the course.
``

or

``
Class average: 60. Your grade: F. You failed the course.
``

## Usage

Import or include the functions in your project. Use the functions to calculate averages, grades, and generate student messages as needed.

## Example

```javascript
const scores = [88, 92, 79, 100, 67];
const studentScore = 85;

console.log(studentMsg(scores, studentScore));
// Output: Class average: 85.6. Your grade: B. You passed the course.
``

## License

This project is open source and free to use.
