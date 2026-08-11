# Project Assignment: Project 02 - Course Registration Simulator

## Overview

Build a command-line Course Registration Simulator in Python. Your program will manage courses, students inside courses, and grades using dictionaries.

This project demonstrates mastery of lists, dictionaries, functions, menus, and file input.

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
- The required functions listed below
- Both required reports
- Follow PEP 8 coding conventions
- Test your code with multiple inputs
- Include the required AI Disclaimer
- Commit and push your work to GitHub
- Submit your GitHub repository URL in Blackboard

### Special late policy

This project uses a lighter late window than the syllabus default: **-10%** if the submission is late but received **before 3/31**. After that date, the usual late policy applies.

### Grading (90% vs above 90%)

| Target | What it means |
|--------|----------------|
| Up to **90%** | Meet all Core Requirements and run correctly (no crashes on bad input, other than the allowed `ValueError` case below) |
| **Above 90%** | Also extend the assignment in some meaningful way while still completing all core requirements |

If you are aiming for above 90%, you must list your extra features as `Additional requirements:` in **two** places:

- At the top of your `project02.py` file
- In your Blackboard submission text

Use your creativity. A few extension ideas (you are not limited to these):

- Save/load full data: save the full `courses` structure (including students and grades) to a file and load it back later (JSON recommended)
- Stronger input validation: keep asking until valid instead of returning to the menu
- Better reports: alphabetical rosters, averages per course, show ungraded students clearly
- More reports: ungraded-students report, course-average report, student-summary report
- Search: partial-match student search across all courses and show where they appear

---

## 📁 File Naming

Submit one Python file named:

| Problem | File Name |
|---------|-----------|
| Course Registration Simulator | `project02.py` |

Place `courses.txt` in the same folder as `project02.py` so your program can load it at startup.

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

### Course Registration Simulator

Build a menu-driven program that keeps running until the user chooses to exit.

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

**Sample menu:**

```text
===== Course Registration Simulator =====
1) Add course
2) Remove course
3) Add student to course
4) Remove student from course
5) Assign grade
6) Reports
7) Exit
```

**Course selection UX (required)**

Any time the user needs to choose a course (add/remove student, assign grade, course roster report, grade report, and similar), your program must:

- Display a numbered list of available courses
- Let the user pick a course by number
- Validate the number (reject invalid choices without crashing)
- If there are no courses yet, print a friendly message and return to the main menu

**2) Course management (required)**

- Add a course (example: course code + course name)
- Remove a course
- When a course is removed, all students and grades inside it are removed too

**3) Students in courses (required)**

- Add a student to a course
- Remove a student from a course
- Prevent duplicates within the same course (do not add the same student name twice to the same course)

Do not worry about matching names uniquely across courses. For example, `"Alex Lee"` in `"physics"` does not have to be treated as the same person as `"Alex Lee"` in `"history"`.

**4) Grades (required)**

- Assign a grade to a student for a specific course
- A grade can be a numeric grade in the range **0–100**
- Your program must reject invalid grades
- If a student is in a course but does not have a grade yet, store `None`

**5) Load courses from a file (required)**

Your program must load the list of available courses from a text file when it starts.

File format (required): one line per class (course name).

Example file (`courses.txt`), placed in the same folder as `project02.py`:

```text
physics
history
CPSI-17503
```

Rules:

- Ignore blank lines
- Course names may have spaces (use the entire line)
- If the file is missing, start with no courses and show a friendly message stating that `courses.txt` is missing

You are only required to load course names at startup. You do not have to write changes back to `courses.txt`.

#### Required functions (minimum)

You must implement at least these functions (you can add more):

| Function | What it does |
|----------|----------------|
| `display_menu()` | Prints the menu |
| `add_course(courses, course_name)` | Modifies `courses` |
| `remove_course(courses, course_name)` | Modifies `courses` |
| `add_student_to_course(courses, course_name, student_name)` | Adds the student to the course with grade `None` |
| `remove_student_from_course(courses, course_name, student_name)` | Removes the student from the course |
| `assign_grade(courses, course_name, student_name, grade)` | Stores or updates a grade for a student in a course |
| `load_courses(filename)` | Reads the course file and returns the initial `courses` dictionary |
| `get_course_name(courses)` | Prints a numbered list of courses, prompts the user to select one by number, and returns the selected course name (or `None` if there are no courses) |

#### Recommended data storage

Use dictionaries as your primary data structure for course/student/grade data. Use lists where helpful (menus, building reports, temporary collections).

Shape the nested dictionary like this:

```py
courses = {
    "physics": {"bob smith": 76, "ann wilson": None},
    "history": {"bob smith": 99},
}
```

Meaning:

- Top-level keys are course names (or course codes if you prefer)
- Each course maps to a dictionary of student name → grade
- `None` means the student is enrolled, but not graded yet

How operations map to this structure:

- Add course: `courses[new_course] = {}`
- Remove course: `del courses[course]` or `courses.pop(course)`
- Add student to course: `courses[course][student_name] = None`
- Remove student from course: `del courses[course][student_name]` or `courses[course].pop(student_name)`
- Assign grade: `courses[course][student_name] = grade`

Membership checks you will use a lot:

- Course exists: `if course_name in courses:`
- Student is in a course: `if student_name in courses[course_name]:`

#### Reports (required)

You must implement both of the following:

1. **Grade report for a course:** The user selects a course (from a numbered menu) and sees a list of all students in the course along with their current grades (or `None` / ungraded if not assigned yet).
2. **Student schedule and grades report:** The user enters a student name and the program shows all courses that student is enrolled in, plus their grades in each course (or `None` / ungraded if not yet assigned).

#### Input validation (required)

Your program must handle the following without crashing:

- Invalid menu choice
- Invalid course number (when picking from a numbered course list)
- Unknown student in that course
- Duplicate student name within a course (tell the user there is already a student with that name)
- Invalid grade input (it does not have to be an `int`, but it must represent a number in the range 0–100)

It is OK if nonnumeric grade input causes a `ValueError`, but everything else should be handled without crashing. Handling nonnumeric grade input is a good extension.

#### Example program flow (assign grade)

```text
Choose a course:
1) physics
2) history
Enter course number: 1
Enter student name: ann wilson
Enter grade (0-100): 88
Saved grade: physics → ann wilson → 88
```

If the user enters an invalid course number, invalid grade, or an unknown student, the program should print a friendly message and return to the menu (or re-prompt if you implemented that extension).

---

## 📤 Submission Instructions

1. Accept the GitHub assignment and create your repo.
2. Write and test `project02.py` (and include `courses.txt` in the same folder).
3. Commit and push your files to GitHub.
4. Copy your GitHub repository URL.
5. Submit the repository URL in Blackboard.

---

## ✅ Submission Checklist

- ☐ Menu loop works and keeps running until exit
- ☐ Can add/remove courses
- ☐ Can add/remove students from a course (no duplicates within a course)
- ☐ Can assign grades (validated)
- ☐ Includes at least 2 reports
- ☐ Loads courses from file on start (one line per class)
- ☐ Uses lists and dictionaries meaningfully
- ☐ Uses required functions
- ☐ Bad input does not break anything
- ☐ If aiming for above 90%, extra features listed as `Additional requirements:` in `project02.py` and in the Blackboard submission
- ☐ Correct file name (`project02.py`)
- ☐ AI Disclaimer included
- ☐ Code follows PEP 8 conventions
- ☐ Code tested with multiple inputs
- ☐ Repository pushed to GitHub
- ☐ Repository URL submitted in Blackboard
