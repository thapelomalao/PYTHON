# Section D: README

## Student Management System

**Python version used:** 3.13

---

## 1. Overview

A Python program for managing student grades. Students can be added, updated, removed, searched, and compared through a simple numbered menu. The program is organised using functions, with input validation and error handling techniques.

The program is interactive: it loops on the main menu until the user chooses **Exit**.

---

## 2. Menu Options

| No. | Option | Description |
|-----|--------|-------------|
| 1 | Add a new student | Asks for a name and all subject grades. |
| 2 | Update an existing student's grades | Updates all grades for a student who already exists. |
| 3 | Remove a student | Deletes the student by name. |
| 4 | Search for a student | Shows the student's grades per subject and their average. |
| 5 | View subject-specific grades | Chooses a subject by number and lists every student's grade for it. |
| 6 | View full class summary and report | Displays totals, averages, highest/lowest, and a summary table of the student data that was entered. |
| 7 | Exit | Ends the program. |

---

## 3. Data Structure (Section D)

The data structure used is a **dictionary**:

- **Keys:** student names
- **Values:** grades

Why a dictionary:

1. It gives fast lookups by name for search, update and remove.
2. It keeps grades labelled by subject.

---

## 4. Error Handling

To prevent errors when the user enters the wrong data type or an unexpected value, the code uses `try` and `except ValueError` blocks. These make sure the user enters valid input.

An example of where this is enforced is in the `get_valid_grade` function. Thee code snippet is here:
def get_valid_grade(student_name, subject):
    """function to get a validated grade from the user."""
    while True:
        try:
            grade = float(input(f"Enter {student_name}'s grade for {subject} (0-100): "))
            if 0 <= grade <= 100:
                return grade
            print("Grade must be between 0 and 100.")
        except ValueError:
            print("Please enter a valid number.")
