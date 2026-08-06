# Practice Assignment: Module 8 - File IO

## Overview

This assignment provides an opportunity to apply the concepts covered in this module by writing Python programs that read and write files, handle paths and errors, and persist data.

You will complete:

- One problem from Section 1 – Reading Text Files
- One problem from Section 2 – Writing, Paths, and Error Handling
- One problem from Section 3 – Persistence and Serialization

---

## ▶️ Start Here

Before you begin, watch the walkthrough video below for guidance on how to approach this assignment.

*[Insert walkthrough video about completing programming assignments]*

---

## 🚀 GitHub Classroom

Open the GitHub Classroom assignment using the link below.

**GitHub Classroom Assignment**

[INSERT ASSIGNMENT LINK]

> WARNING: Submit the **repository** URL in the LMS (Blackboard), not a Codespaces / `github.dev` link (those are private to you).

---

## 📋 Assignment Requirements

Complete:

- One problem from Section 1 – Reading Text Files
- One problem from Section 2 – Writing, Paths, and Error Handling
- One problem from Section 3 – Persistence and Serialization
- Follow PEP 8 coding conventions
- Test your code with multiple inputs (including missing files and bad data)
- Include the required AI Disclaimer
- Commit and push your work to GitHub
- Submit your GitHub repository URL in Blackboard

---

## 📁 File Naming

Each problem should be saved as a separate Python file.

| Problem | File Name |
|---------|-----------|
| Line Stats Report | `program1a.py` |
| Keyword Highlighter | `program1b.py` |
| Simple CSV Exporter | `program2a.py` |
| Number File Analyzer + Writer | `program2b.py` |
| Pickle Notes App | `program3a.py` |
| Persistent Counter | `program3b.py` |

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

### Section 1 - Reading Text Files (Choose One)

#### Problem 1a: Line Stats Report

Create a program that reads a text file and prints a short report about it.

**Requirements:**

- Ask the user for a filename to analyze
- Use `with open(...)` to open and read the file
- Read the file **line-by-line** (loop over the file object)
- Print:
  - total number of lines
  - number of non-empty lines (after `strip()`)
  - longest line length (after removing the trailing newline)
- If the file does not exist, print a friendly error message and exit cleanly (no crash)

#### Problem 1b: Keyword Highlighter

Create a program that searches a text file for a keyword.

**Requirements:**

- Ask the user for:
  - a filename
  - a keyword
- Read line-by-line and print only the matching lines
- Output format must include a line number, like:
  - `12: This is the matching line...`
- Matching must be **case-insensitive**
- If there are no matches, print: `No matches found.`
- Handle missing file with a friendly message (no crash)

---

### Section 2 - Writing, Paths, and Error Handling (Choose One)

#### Problem 2a: Simple CSV Exporter

Create a program that collects small contact cards from the user and writes them to a file.

**Requirements:**

- Ask the user for:
  - output filename (example: `contacts.csv`)
  - then repeatedly ask for `name`, `email`, `age`
  - stop when the user types `"done"` for the name
- Write a CSV-like file with this exact header:
  - `name,email,age`
- Each contact should be written on its own line (example: `Ada Lovelace,ada@ualr.edu,19`)
- Validate `age` so the program does not crash on bad input
- Use **write mode** (`'w'`) and `with open(...)`
- Use `os.path.join(...)` to build the output path in a `data` folder:
  - If the folder does not exist, create it first (hint: `os.makedirs(..., exist_ok=True)`)

#### Problem 2b: Number File Analyzer + Writer

Create a program that reads a file containing one number per line, computes statistics, and writes a report file.

**Requirements:**

- Ask the user for:
  - an input filename (to read numbers from)
  - an output filename (where to write the report)
- Read line-by-line
- Ignore blank lines
- If a line is not a valid number, **skip it** and keep going (no crash)
- After reading, compute:
  - count of valid numbers
  - sum
  - average (rounded to 2 decimals) only if count > 0
  - min and max only if count > 0
- **Write these results to the output file** in a clear report format
- If there were no valid numbers, write a message like "No valid numbers found."
- Handle missing input file with a friendly message (no crash)

---

### Section 3 - Persistence and Serialization (Choose One)

#### Problem 3a: Pickle Notes App

Make a tiny notes app that saves and loads your notes between runs.

**Requirements:**

- Notes are stored as a list of strings
- On startup:
  - if `notes.pkl` exists, load it
  - otherwise start with an empty list
- Show a simple menu loop:
  1. Add note
  2. List notes
  3. Delete note (by number)
  4. Quit (save automatically)
- Use `pickle` to save/load the notes list
- Handle invalid menu choices and invalid delete numbers without crashing

#### Problem 3b: Persistent Counter

Make a program that keeps counts of words across multiple runs.

**Requirements:**

- Use a dictionary `{word: count}`
- On startup:
  - load from `counter.pkl` if it exists
  - otherwise start empty
- Repeatedly ask the user for a word:
  - entering `"done"` exits
  - otherwise update the counter for that word (case-insensitive)
- At the end, print the top 5 most common words (or fewer if there aren't 5)
- Save the updated dictionary back to `counter.pkl`

---

## 📤 Submission Instructions

1. Complete the required programming problems.
2. Commit and push your files to GitHub.
3. Copy your GitHub repository URL.
4. Submit the repository URL in Blackboard.

---

## ✅ Submission Checklist

- ☐ Completed one Reading Text Files problem
- ☐ Completed one Writing, Paths, and Error Handling problem
- ☐ Completed one Persistence and Serialization problem
- ☐ Correct file names
- ☐ AI Disclaimer included
- ☐ Code follows PEP 8 conventions
- ☐ Code tested with multiple inputs
- ☐ Repository pushed to GitHub
- ☐ Repository URL submitted in Blackboard
