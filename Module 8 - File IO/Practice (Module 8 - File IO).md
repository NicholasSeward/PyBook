# Practice Assignment: Module 8 - File I/O

## Overview

Complete **3 problems total** — choose **1 from each section** below. Each section focuses on different aspects of file I/O in Python.

## Instructions

- Choose **1 problem from Section 1** (Reading text files)
- Choose **1 problem from Section 2** (Writing + paths + error handling)
- Choose **1 problem from Section 3** (Persistence + serialization)
- Use proper PEP 8 coding conventions
- Test your code with different inputs (including missing files and bad data)

## GitHub Classroom Link (Get Started)

Accept the assignment here:

👉 **[INSERT GITHUB CLASSROOM LINK HERE]**

## File Naming and Submission

### File Naming

Each problem should be a separate file:

- `program1a.py` 
- `program1b.py`
- `program2a.py`
- `program2b.py`
- `program3a.py`
- `program3b.py`

### AI Disclaimer Requirement

**CRITICAL:** Each file must include an AI Disclaimer at the top. The autograder will look for this exact text and check the content after it.

### Submission Process

1. Create your program files
2. Test your code thoroughly
3. Commit and push to GitHub
4. Submit your repository URL

**Example repository URL:** `https://github.com/Seward-Classes/practice-08-username`

---

## Section 1: Reading Text Files (Choose 1)

### Problem 1a: Line Stats Report

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

---

### Problem 1b: Keyword Highlighter

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

## Section 2: Writing + Paths + Error Handling (Choose 1)

### Problem 2a: Simple CSV Exporter

Create a program that collects small “contact cards” from the user and writes them to a file.

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

---

### Problem 2b: Number File Analyzer + Writer

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
  - average (rounded to 2 decimals) — only if count > 0
  - min and max — only if count > 0
- **Write these results to the output file** in a clear report format, for example:
- If there were no valid numbers, write a message like “No valid numbers found.”
- Handle missing input file with a friendly message (no crash)

---

## Section 3: Persistence + Serialization (Choose 1)

### Problem 3a: Pickle Notes App

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

---

### Problem 3b: Persistent Counter

Make a program that keeps counts of words across multiple runs.

**Requirements:**

- Use a dictionary `{word: count}`
- On startup:
  - load from `counter.pkl` if it exists
  - otherwise start empty
- Repeatedly ask the user for a word:
  - entering `"done"` exits
  - otherwise update the counter for that word (case-insensitive)
- At the end, print the top 5 most common words (or fewer if there aren’t 5)
- Save the updated dictionary back to `counter.pkl`

