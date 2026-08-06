# Practice Assignment: Module 12 - Fancy Data Structures

## Overview

This assignment provides an opportunity to apply the concepts covered in this module by writing short Python programs with linked lists and binary search trees.

You will complete:

- One problem from Section 1 – Linked Lists
- One problem from Section 2 – Binary Search Trees

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

- One problem from Section 1 – Linked Lists
- One problem from Section 2 – Binary Search Trees
- Follow PEP 8 coding conventions
- Test your code with multiple inputs
- Include the required AI Disclaimer
- Commit and push your work to GitHub
- Submit your GitHub repository URL in Blackboard

---

## 📁 File Naming

Each problem should be saved as a separate Python file.

| Problem | File Name |
|---------|-----------|
| Build and Traverse | `program1a.py` |
| Insert at Front | `program1b.py` |
| Insert and Search | `program2a.py` |
| In-Order Print | `program2b.py` |

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

### Section 1 - Linked Lists (Choose One)

#### Problem 1a: Build and Traverse

Create a simple singly linked list and print its values.

**Requirements:**

- Define a `Node` class with `data` and `next`
- Build a list with at least **5** nodes (you may hardcode the values)
- Write a function `traverse(head)` that walks the list and prints each value on one line (or separated by spaces)
- Call `traverse` from `main` (or the bottom of your file)

**Sample Output:**

```text
10 20 30 40 50
```

#### Problem 1b: Insert at Front

Build a linked list by always inserting new values at the **front**.

**Requirements:**

- Define a `Node` class with `data` and `next`
- Write a function `insert_front(head, value)` that returns the new head
- Ask the user for integers until they type `done`
- Insert each integer at the front of the list
- Print the final list from head to end (order will be reverse of entry order)

**Sample Output:**

```text
Enter an integer (or 'done'): 1
Enter an integer (or 'done'): 2
Enter an integer (or 'done'): 3
Enter an integer (or 'done'): done
List: 3 -> 2 -> 1
```

---

### Section 2 - Binary Search Trees (Choose One)

#### Problem 2a: Insert and Search

Create a minimal BST that can insert values and search for a value.

**Requirements:**

- Define a `Node` class with `value`, `left`, and `right`
- Write `insert(root, value)` that inserts into a BST (return the root)
- Write `contains(root, value)` that returns `True` if the value is in the tree
- Insert these values in order: `8, 3, 10, 1, 6`
- Ask the user for a number and print whether it is in the tree

**Sample Output:**

```text
Enter a number to search: 6
Found: True

Enter a number to search: 7
Found: False
```

(You may ask once, or loop until `done`.)

#### Problem 2b: In-Order Print

Build a BST and print values in sorted order using an in-order traversal.

**Requirements:**

- Define a `Node` class with `value`, `left`, and `right`
- Write `insert(root, value)` for a BST
- Write `inorder(root)` that prints values from smallest to largest
- Insert: `8, 3, 10, 1, 6, 14, 4, 7`
- Call `inorder` and print the sorted sequence

**Sample Output:**

```text
1 3 4 6 7 8 10 14
```

---

## 📤 Submission Instructions

1. Complete the required programming problems.
2. Commit and push your files to GitHub.
3. Copy your GitHub repository URL.
4. Submit the repository URL in Blackboard.

---

## ✅ Submission Checklist

- ☐ Completed one Linked Lists problem
- ☐ Completed one Binary Search Trees problem
- ☐ Correct file names
- ☐ AI Disclaimer included
- ☐ Code follows PEP 8 conventions
- ☐ Code tested with multiple inputs
- ☐ Repository pushed to GitHub
- ☐ Repository URL submitted in Blackboard
