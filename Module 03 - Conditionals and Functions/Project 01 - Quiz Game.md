# Project Assignment: Project 01 - Quiz Game

## Overview

Build a command-line quiz program in Python. This project demonstrates mastery of Module 1–3 concepts: input/output, variables and types, boolean logic, selection, functions, scope, and truthy/falsy checks.

You will complete **one** of the following project styles:

- **Option A (Scored Quiz):** Grade answers as correct/incorrect and report the user’s score and number correct.
- **Option B (Classification Quiz):** Determine a category result (example: “Which Harry Potter House are you?”) where answers meaningfully contribute to the final category.

**Determinism requirement (CRITICAL):** Two runs with the same answers must produce the same result. Do not use randomness.

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

- One project style: Option A (Scored Quiz) **or** Option B (Classification Quiz)
- All Core Requirements listed below
- Follow PEP 8 coding conventions
- Test your code with multiple inputs
- Include the required AI Disclaimer
- Commit and push your work to GitHub
- Submit your GitHub repository URL in Blackboard

### Learning objectives (Module 1–3)

This project should use:

- **Input/Output:** `input()`, `print()`, f-strings
- **Variables and types:** storing values, type conversion where needed
- **Boolean logic:** comparisons, `and` / `or` / `not`
- **Selection:** `if` / `elif` / `else`
- **Functions:** defining/calling functions, parameters, return values
- **Scope:** local vs global variables (avoid globals when possible)
- **Truthy/Falsy:** clean checks such as `if not name:`

### Core requirements (both options)

Your program must:

- Ask at least **6** questions (the user must enter an answer for each)
- Use `if`/`elif`/`else` meaningfully (not just a single `if`)
- Use boolean logic at least once (example: `and`, `or`, `not`)
- Print a final summary at the end (score report or classification result)
- Be deterministic: same answers → same output every time

Loops are **not** required. If you know them, you may use them, but you do not need them for a complete submission.

### Grading (90% vs above 90%)

| Target | What it means |
|--------|----------------|
| Up to **90%** | Meet all Core Requirements and all requirements for Option A or Option B |
| **Above 90%** | Also extend the assignment in some meaningful way while still completing all core requirements |

One example extension is input validation (loop until the user types a valid answer). Other creative extensions are welcome. Use your creativity and extend the project in a way that is interesting to you.

---

## 📁 File Naming

Submit one Python file named:

| Problem | File Name |
|---------|-----------|
| Quiz Game (Option A or B) | `project01.py` |

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

### Choose One Option

#### Option A: Scored Quiz (Correct / Incorrect)

Build a themed quiz that grades each answer and reports a score.

**Requirements (Option A):**

In addition to the Core Requirements:

1. Track `total_questions` and `num_correct`.
2. Compute a percentage score (for example: `(num_correct / total_questions) * 100`).
3. Print a final report that includes number correct, total questions, and percent score.
4. Have a theme. Do not use a pile of unrelated random questions.
5. Give a message based on the quiz results.

**Example Final Report (Option A):**

```text
===== QUIZ RESULTS =====
Correct: 5 / 6
Score: 83.33%
Almost Perfect!
========================
```

**Sample Interaction (Option A):**

```text
Welcome to Project 01: Quiz Game!

Q1) What does `==` do in Python?
A) Assigns a value
B) Compares two values
C) Creates a function
D) Ends a program
Your answer (A/B/C/D): b
Correct!

...

===== QUIZ RESULTS =====
Correct: 6 / 6
Score: 100.00%
Perfection
========================
```

#### Option B: Classification Quiz (Category Result)

Build a quiz that maps answers into categories and reports a final category.

**Requirements (Option B):**

In addition to the Core Requirements:

1. Have at least **3** possible categories (example: Gryffindor / Ravenclaw / Hufflepuff / Slytherin).
2. Each answer must add points (or otherwise contribute) to at least one category in a meaningful way.
3. At the end, compute the category with the highest total.
4. Tie handling must be deterministic (**CRITICAL**). Choose one:
   - Add a final tie-breaker question that only runs when there is a tie, or
   - Use a fixed tie-break rule (example: “If tied, pick the category that comes first alphabetically.”)
5. Print a final report that includes:
   - Final category
   - A short explanation (1–2 sentences) describing what that category means

**Example Final Report (Option B):**

```text
===== RESULTS =====
House: Ravenclaw
You value curiosity, learning, and creative problem-solving.
===================
```

**Sample Interaction (Option B):**

```text
Welcome to the Sorting Quiz!

Q1) Pick a weekend activity:
A) Read a book
B) Lead a group project
C) Practice a skill
D) Try something risky
Your answer (A/B/C/D): A

...

===== RESULTS =====
House: Ravenclaw
You value curiosity, learning, and creative problem-solving.
===================
```

---

## 📤 Submission Instructions

1. Write and test `project01.py` locally (or in Codespaces).
2. Commit and push your file to GitHub.
3. Copy your GitHub repository URL.
4. Submit the repository URL in Blackboard.

---

## ✅ Submission Checklist

- ☐ Completed Option A **or** Option B
- ☐ At least 6 questions
- ☐ Uses `if`/`elif`/`else` and boolean logic
- ☐ Final summary prints score or classification
- ☐ Deterministic (no randomness; Option B ties handled deterministically)
- ☐ If aiming for above 90%, includes a meaningful extension (example: input validation)
- ☐ Correct file name (`project01.py`)
- ☐ AI Disclaimer included
- ☐ Code follows PEP 8 conventions
- ☐ Code tested with multiple inputs
- ☐ Repository pushed to GitHub
- ☐ Repository URL submitted in Blackboard
