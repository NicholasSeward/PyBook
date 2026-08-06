# Practice Assignment: Module 11 - Python Tricks

## Overview

This assignment provides an opportunity to apply the concepts covered in this module by writing Python programs using sets, comprehensions, `zip`, lambdas, and related idioms.

You will complete:

- Any 3 of the 7 challenges below

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

- Any 3 of the 7 challenges below
- Follow PEP 8 coding conventions
- Test your code with multiple inputs (programs must not crash on bad input)
- Include the required AI Disclaimer
- Commit and push your work to GitHub
- Submit your GitHub repository URL in Blackboard

---

## 📁 File Naming

Each challenge should be saved as a separate Python file. Use **Challenge N → `programN.py`**.

| Challenge | File Name |
|-----------|-----------|
| Dedup + Fast Membership + Stable Output | `program1.py` |
| Filter + Map Without Loops | `program2.py` |
| Build an Index (Enumerate + Dict Comprehension) | `program3.py` |
| Pair Up Two Lists (Zip + Sorting with lambda) | `program4.py` |
| Password Rules Checker (any/all + Generator Expressions) | `program5.py` |
| Frequency Report (Counter + f-string formatting) | `program6.py` |
| Grouping Tool (defaultdict + Slicing) | `program7.py` |

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

#### Problem 1: Dedup + Fast Membership + Stable Output

**Required tricks:** set, sorted (or sorting), membership testing with `in`

Write a program that:

- Asks the user to enter words (one per line) until they type `done`
- Prints:
  - Total number of words entered
  - Number of unique words
  - A **sorted** list of the unique words (alphabetical)
- Then asks the user for a word to search and prints whether it is in the unique set

**Must-haves:**

- Use a **set** for membership testing
- Output the unique words in a deterministic order (sorted)

#### Problem 2: Filter + Map Without Loops

**Required tricks:** list comprehension, optional: f-strings

Write a program that:

- Asks the user to input 5 numbers, one at a time, using a list comprehension (`int(input(f"num{i+1}: "))` as a hint)
- Creates and prints:
  - A list of squares of the **even** numbers
  - A list of the numbers that are **multiples of 3**
  - A list of strings like `"17 -> odd"` or `"20 -> even"` for every number

**Must-haves:**

- Use **at least 3** list comprehensions (including the initial input step)

#### Problem 3: Build an Index (Enumerate + Dict Comprehension)

**Required tricks:** `enumerate`, dict comprehension

Write a program that:

- Has this list:
  - `items = ["alpha", "beta", "gamma", "delta", "epsilon"]`
- Builds a dictionary mapping each item to its index (example: `"beta" -> 1`)
- Then repeatedly asks the user for an item name and prints its index
  - Stops when the user types `done`

**Must-haves:**

- Build the dictionary using a **dict comprehension** and **enumerate**
- Handle unknown items with a friendly message (no crash)

#### Problem 4: Pair Up Two Lists (Zip + Sorting with lambda)

**Required tricks:** `zip`, `sorted(..., key=lambda ...)`

Write a program that:

- Has these lists:
  - `movies = ["Inception", "The Matrix", "Interstellar", "Parasite"]`
  - `ratings = [8.8, 8.7, 8.6, 8.6]`
- Combines them into a list of dictionaries like:
  - `{"movie": "Inception", "rating": 8.8}`
- Prints a leaderboard (highest rating first). If ratings tie, sort by movie title A-Z.

**Must-haves:**

- Combine using **zip**
- Sort using **sorted** with a **lambda key**

#### Problem 5: Password Rules Checker (any/all + Generator Expressions)

**Required tricks:** `any`, `all`, generator expressions

Write a program that:

- Asks the user to enter passwords until they type `done`
- For each password, print whether it passes ALL of these rules:
  - length >= 8
  - contains **at least one digit**
  - contains **at least one uppercase** letter
  - contains **at least one** of these symbols: `! @ # $`

**Must-haves:**

- Use **any/all** with generator expressions (not manual loops) to check the rules
- Print a short reason when it fails (example: "Missing digit")

#### Problem 6: Frequency Report (Counter + f-string formatting)

**Required tricks:** `collections.Counter`, f-strings with format specs

Write a program that:

- Uses this text (hardcode it in your file as a triple-quoted string):
  - Choose a chapter from a public domain book. Here are two options:
    - **Option 1:** Chapter 1 of "Pride and Prejudice" by Jane Austen ([Gutenberg Link](https://www.gutenberg.org/files/1342/1342-h/1342-h.htm#chap01))
    - **Option 2:** Chapter 1 of "The Adventures of Sherlock Holmes" by Arthur Conan Doyle ([Gutenberg Link](https://www.gutenberg.org/files/1661/1661-h/1661-h.htm#chap01))
  - You may pick and copy the text from one of these sources, or another public domain book of your choice. (Project Gutenberg is a great resource: [https://www.gutenberg.org/](https://www.gutenberg.org/))
- Counts the frequency of each word (case-insensitive)
- Prints:
  - The 10 most common words (or fewer if there aren't 10)
  - Each line should be nicely formatted with aligned columns, like:
    - `word: count`

**Must-haves:**

- Use `Counter(...)`
- Use an f-string format spec to line up output (example: fixed width for the word column)

#### Problem 7: Grouping Tool (defaultdict + Slicing, with user input)

**Required tricks:** `collections.defaultdict(list)`, slicing

Write a program that:

- Asks the user to enter category/item pairs (example: `fruit apple`), one per line
- End input by typing `done`
- Groups items by category into a dictionary like:
  - `{"fruit": ["apple", "banana"], "veg": ["carrot"]}`
- For each category, print:
  - the category name, the number of items, and the list of items
  - If there are more than 3 items in a category, show only the first 3 items followed by `...`

**Example output:**

```text
fruit (3): apple, banana, orange
veg (2): carrot, spinach
snacks (5): chips, cookies, popcorn, ...
```

**Must-haves:**

- Use `defaultdict(list)` to build the groups
- Use slicing (like `items[:3]`) in your output

---

## 📤 Submission Instructions

1. Complete the required programming problems.
2. Commit and push your files to GitHub.
3. Copy your GitHub repository URL.
4. Submit the repository URL in Blackboard.

---

## ✅ Submission Checklist

- ☐ Completed 3 of 7 challenges
- ☐ Used the required Python tricks for each chosen challenge
- ☐ Correct file names (`programN.py` matching challenge numbers)
- ☐ AI Disclaimer included
- ☐ Code follows PEP 8 conventions
- ☐ Code tested with multiple inputs
- ☐ Repository pushed to GitHub
- ☐ Repository URL submitted in Blackboard
