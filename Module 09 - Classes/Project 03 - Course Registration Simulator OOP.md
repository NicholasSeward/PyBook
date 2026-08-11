# Project Assignment: Project 03 - Course Registration Simulator (OOP)

## Overview

Build a command-line Course Registration Simulator in Python, redesigned with object-oriented programming (OOP). Your program will manage courses, students inside courses, and grades.

This project is based on the idea of Project 02, but this time you must use classes and objects to organize the data and behavior.

---

## ▶️ Start Here

Before you begin, watch the walkthrough video below for guidance on how to approach this assignment.

*[Insert walkthrough video about completing programming projects]*

---

## 🚀 GitHub

Open the GitHub assignment using the link below.

**GitHub Assignment**

[INSERT ASSIGNMENT LINK]

> WARNING: Submit the **repository** URL in the LMS (Blackboard), not a Codespaces / `github.dev` link (those are private to you).

---

## 📋 Assignment Requirements

Complete:

- All Core Requirements listed below
- The required classes and program-level functions
- Both required reports
- Follow PEP 8 coding conventions
- Test your code with multiple inputs
- Include the required AI Disclaimer
- Commit and push your work to GitHub
- Submit your GitHub repository URL in Blackboard

### Grading (90% vs above 90%)

| Target | What it means |
|--------|----------------|
| Up to **90%** | Meet all Core Requirements and run correctly (no crashes on bad input) |
| **Above 90%** | Also extend the assignment in some meaningful way while still completing all core requirements |

If you are aiming for above 90%, you must list your extra features as `Additional requirements:` in **two** places:

- At the top of your `project03.py` file
- In your Blackboard submission text

Use your creativity. A few extension ideas (you are not limited to these):

- Better reports: alphabetical rosters, averages per course, show ungraded students clearly
- More reports: ungraded-students report, course-average report, student-summary report
- Search: partial-match student search across all courses and show where they appear
- Cleaner architecture: additional helper classes (like `ReportBuilder`) while still keeping I/O separate

---

## 📁 File Naming

Submit one Python file named:

| Problem | File Name |
|---------|-----------|
| Course Registration Simulator (OOP) | `project03.py` |

Your program should create and use `data.pkl` in the same folder as `project03.py`.

---

## 🤖 AI Usage Disclosure

**CRITICAL:** Each Python file must begin with an AI Disclaimer. The autograder will look for this exact text and check the content after it.

Choose the statement that best reflects how AI was (or was not) used while completing your assignment.

### Examples of AI Disclaimers (choose the most appropriate or write your own)

**No AI Use:**

```text
# AI Disclaimer: This code was written without the use of AI tools.
# Any assistance received was from course materials, textbooks, or instructor guidance only.
```

**Minimal AI Use (e.g., syntax help, debugging):**

```text
# AI Disclaimer: This code was written with minimal AI assistance.
# Used AI for: syntax checking and debugging only.
# Core logic and problem-solving approach are my own work.
```

**Moderate AI Use (e.g., code structure, algorithm suggestions):**

```text
# AI Disclaimer: This code was written with moderate AI assistance.
# Used AI for: code structure suggestions and algorithm guidance.
# I implemented the solutions and modified the AI suggestions to fit the requirements.
```

**Extensive AI Use (e.g., significant code generation):**

```text
# AI Disclaimer: This code was written with extensive AI assistance.
# Used AI for: code generation, debugging, and optimization.
# I reviewed, tested, and modified all AI-generated code to ensure it meets requirements.
```

**Unacceptable AI Use (e.g., "vibe coding" without learning):**

```text
# AI Disclaimer: This code was written with extensive AI assistance.
# Used AI for: complete code generation to pass autograder.
# I copied the code without understanding it, just to get a green checkmark.
# I didn't actually learn anything from this assignment.
```

Your program code starts here...

---

## 💻 Programming Problems

### Course Registration Simulator (OOP)

Build a menu-driven program that keeps running until the user chooses to exit. Organize data and behavior with classes. Keep all user I/O in functions outside those classes.

#### Core requirements

**1) Menu loop (required)**

Display a menu and keep running until the user chooses to exit.

At minimum, include menu options for:

- Add a course
- Remove a course
- Add a student to a course
- Remove a student from a course
- Assign a grade to a student in a course
- View reports
- Exit

**2) Course selection UX (required)**

Any time the user needs to choose a course (add/remove student, assign grade, reports, and similar), your program must:

- Display a numbered list of available courses
- Let the user pick a course by number
- Validate the number (reprompt until valid; do not crash)
- If there are no courses yet, print a friendly message and return to the main menu

**3) Student selection UX (required)**

Any time the user needs to choose a student within a course (remove student, assign grade, and similar), your program must:

- Display a numbered list of students currently enrolled in that course
- Let the user pick a student by number
- Validate the number (reprompt until valid; do not crash)
- If the selected course has no students, print a friendly message and return to the main menu

**4) Course management (required)**

- Add a course (course name or code is fine)
- Remove a course
- When a course is removed, all students and grades inside it are removed too

**5) Students in courses (required)**

- Add a student to a course
- Remove a student from a course
- Prevent duplicates within the same course (do not add the same student name twice to the same course)

**6) Grades (required)**

- Assign a grade to a student for a specific course
- A grade must be a number in the range **0–100**
- Reject invalid grades without crashing
- If a student is in a course but does not have a grade yet, store it as ungraded (`None` recommended)

**7) Load all data from a file (required)**

Load all course and student data when the program starts so users can continue where they left off.

Recommended approach: use the Python `pickle` module to save and reload the entire courses/students/grades structure.

Other options: JSON or YAML. If you choose JSON or YAML, you must write your own serializers and deserializers to convert objects (like `Course` and `Student`) to and from dictionaries, lists, or other serializable types. `pickle` is recommended because it handles most Python objects automatically.

How to use `pickle` (`data.pkl` suggested):

- When the program starts, try to load all data from `data.pkl`
- If the file exists, restore the full state (all courses, enrolled students, grades)
- If the file is missing, initialize with no courses and show a friendly message (example: `data.pkl not found. Starting with no courses.`)
- When the user exits, save all current state back to `data.pkl`

Starter pattern:

```py
import pickle
import os

DATA_FILE = "data.pkl"

def load_data(filename):
    if os.path.exists(filename):
        with open(filename, "rb") as f:
            return pickle.load(f)
    print(f"{filename} not found. Starting with no courses.")
    return None  # main should start from scratch

def save_data(filename, data):
    with open(filename, "wb") as f:
        pickle.dump(data, f)
```

#### OOP design (required)

**No I/O inside objects**

Inside your classes, you must **not** use `input()` or `print()`.

Objects should do work and return results, not talk to the user.

The only UI-like method allowed in objects is `__str__` (which returns a string). Even in `__str__`, do not call `print()`. The caller can print the returned string.

**Why we keep I/O out of objects**

- **Separation of concerns:** Objects should model data and behavior, not user interaction.
- **Testing:** Methods that print or call `input()` are harder to test. Pure methods can be tested with normal function calls.
- **Reusability:** If objects do not depend on the console, you can reuse them in a GUI, web app, or different project.
- **Cleaner code:** The UI layer (menus and prompts) can change without rewriting your model layer (classes).

In short: classes should compute and return results; separate functions should handle user interaction.

**Required classes (minimum)**

You must implement at least these classes (you may add more).

##### `Student`

Represents a student inside a course. This keeps the "names do not have to match across courses" rule simple.

Minimum attributes:

- `name` (string)
- `grade` (number 0–100, or `None` for ungraded)

Minimum behavior:

- `set_grade(grade)` → validates and stores the grade
- `is_graded()` → returns `True` / `False`
- `__str__()` → returns a readable line like `"Ann Wilson: 88"` or `"Ann Wilson: ungraded"`

##### `Course`

Represents one course and the students enrolled in it.

Minimum attributes:

- `name` (string)
- a collection of students (recommended: dictionary keyed by a normalized name)

Minimum behavior:

- `add_student(student_name)` → enrolls a student (no duplicates)
- `remove_student(student_name)` → removes a student
- `assign_grade(student_name, grade)` → updates that student’s grade
- `roster()` → returns a list of `Student` objects (for reporting)
- `__str__()` → returns a readable course summary (course name + enrollment count)

##### `Registrar`

Represents the system that holds all courses.

Minimum attributes:

- a collection of courses (recommended: dictionary keyed by a normalized course name)

Minimum behavior:

- `add_course(course_name)`
- `remove_course(course_name)`
- `get_course(course_name)` → returns the `Course` or `None`
- `list_courses()` → returns a list of course names (for numbered menus)
- `student_schedule(student_name)` → returns the student’s courses and grades across all courses as a list of tuples, for example `[("Physics", 90), ("Chemistry", None)]` where each tuple is `(course_name, grade)`

#### Required program-level functions (not methods)

Your UI and file operations should be in functions outside the classes. You must implement at least these (you can add more):

| Function | What it does |
|----------|----------------|
| `display_menu()` | Prints the menu |
| `load_data(filename)` | Returns the data stored in the file |
| `save_data(filename, data)` | Saves data to the file |
| `choose_course(registrar)` | Prints a numbered course list, prompts for a number, loops until valid, returns a `Course` (or `None` only if there are no courses) |
| `choose_student(course)` | Prints a numbered student list, prompts for a number, loops until valid, returns a `Student` (or `None` only if there are no students) |
| `prompt_nonempty(prompt_text)` | Prompts until the user enters non-empty text |
| `prompt_grade()` | Prompts until a valid grade number in 0–100 is entered |
| `main()` | Very small; should mostly call other functions |

**`main()` should be simple (required)**

Your `main()` should mostly:

- create/load the `Registrar`
- run the menu loop
- call helper functions to handle each action

Your `main()` should **not** contain lots of long logic.

#### Suggested I/O helpers (recommended)

These are optional helpers to keep I/O separate and keep your code clean:

- `prompt_nonempty(prompt_text)` → keeps asking until the user enters non-empty text
- `prompt_int(prompt_text, min_value=None, max_value=None)` → reads and validates an integer (reprompts until valid)
- `prompt_float(prompt_text, min_value=None, max_value=None)` → reads and validates a float (reprompts until valid)
- `print_course_list(registrar)` → prints numbered courses (uses `registrar.list_courses()`)
- `print_course_grade_report(course)` → prints a formatted roster using `Student.__str__()`
- `prompt_menu_choice(min_choice, max_choice)` → reprompts until the user enters a number in range

#### Reports (required)

You must implement both of the following:

1. **Grade report for a course:** The user selects a course (numbered menu). The program displays all students in that course and their grades (or `"ungraded"`).
2. **Student schedule and grades report:** The user enters a student name. The program displays all courses that student is enrolled in, plus their grades in each course (or `"ungraded"`).

#### Input validation (required)

Handle every user prompt without crashing. For every prompt (menu choice, course number, student name, grade, and similar), **loop until the user enters something valid**.

Do not give up and go back to the menu just because the user typed something invalid. Keep prompting until they enter a valid value.

Required cases:

- Invalid menu choice
- Invalid course number (when picking from a numbered course list)
- Unknown student in that course
- Duplicate student name within a course
- Invalid grade input (not a number, or outside 0–100)

---

## 📤 Submission Instructions

1. Accept the GitHub assignment and create your repo.
2. Write and test `project03.py` locally (or in Codespaces).
3. Commit and push your file to GitHub.
4. Copy your GitHub repository URL.
5. Submit the repository URL in Blackboard.

---

## ✅ Submission Checklist

- ☐ Menu loop works and keeps running until exit
- ☐ Loads data from file on start and saves on exit
- ☐ Uses OOP design (classes + objects) meaningfully
- ☐ No `input()` / `print()` inside object methods
- ☐ Can add/remove courses
- ☐ Can add/remove students from a course (no duplicates within a course)
- ☐ Can assign grades (validated; reprompt until valid)
- ☐ Includes at least 2 reports
- ☐ Uses required classes and program-level functions
- ☐ `main()` stays small
- ☐ If aiming for above 90%, extra features listed as `Additional requirements:` in `project03.py` and in the Blackboard submission
- ☐ Correct file name (`project03.py`)
- ☐ AI Disclaimer included
- ☐ Code follows PEP 8 conventions
- ☐ Code tested with multiple inputs
- ☐ Repository pushed to GitHub
- ☐ Repository URL submitted in Blackboard
