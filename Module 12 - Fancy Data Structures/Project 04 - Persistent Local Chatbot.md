# Project Assignment: Project 04 - Persistent Local Chatbot

## Overview

Build a command-line chatbot in Python using a local model. You do not train the model. You build the program around it.

Each model call is stateless. Your code supplies memory by keeping a list of messages and passing that list (or a trimmed copy) on every turn.

---

## ▶️ Start Here

Before you begin, watch the walkthrough video below for guidance on how to approach this assignment.

*[Insert walkthrough video about completing programming projects]*

**Python version:** Set the interpreter to **3.12.1** (lower-right of the editor) so the starter will run. The walkthrough video covers this.

Run the starter first so you can see baseline `chat(...)` behavior before you add history, persistence, and commands.

---

## 🚀 GitHub

Open the GitHub assignment using the link below.

**GitHub Assignment**

[INSERT ASSIGNMENT LINK]

> WARNING: Submit the **repository** URL in the LMS (Blackboard), not a Codespaces / `github.dev` link (those are private to you).

The starter repo already has `main.py` wired to the model. Work in `main.py`. That is what will be graded. You may add other files and import them.

---

## 📋 Assignment Requirements

Complete:

- All Core Requirements listed below
- The four required actions (chat, clear, save now, quit)
- Follow PEP 8 coding conventions
- Test your code with multiple inputs
- Include the required AI Disclaimer
- Commit and push your work to GitHub
- Submit your GitHub repository URL in Blackboard

### Grading (90% vs above 90%)

| Target | What it means |
|--------|----------------|
| Up to **90%** | Meet all Core Requirements; no crash on bad input or a bad file; history shape is correct; code is readable |
| **Above 90%** | Also extend the assignment in some meaningful way while still completing all core requirements |

If you are aiming for above 90%, you must list your extra features as `Additional requirements:` in **two** places:

- At the top of your `main.py` file
- In your Blackboard submission text

Use your creativity. A few extension ideas (you are not limited to these):

- Object-oriented design (for example, a `ChatSession` class)
- Multiple save files (switch or create conversations, such as `/switch`)
- Extra commands: `/help`, `/export`, `/transcript`, `/history`, `/undo`, `/redo`
- History trimming (limit conversation length)
- Basic tests for save/load and commands (testing model replies is not required)
- Personas or simple tools (different system messages, or small built-in utilities)

Small local models can be weak at math and non-deterministic. Treat odd answers as a model limitation, not necessarily a bug in your loop.

---

## 📁 File Naming

Work in the starter file:

| Problem | File Name |
|---------|-----------|
| Persistent Local Chatbot | `main.py` |

You may add other files and import them. `main.py` is what will be graded.

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

### Persistent Local Chatbot

The starter provides `chat(...)` that takes a list of dicts, each like `{"role": "user"|"assistant"|"system", "content": "..."}`, and returns the assistant reply string. The exact function name may differ. Follow the starter.

#### Core requirements

**1) Session loop**

Use a `while` loop until the user quits.

Each chat turn:

1. `input()`
2. Append the user message
3. Call `chat` with history
4. Append the assistant message
5. Print the reply (for example `AI: ...`)

**2) Message history**

History is a list of dicts with at least `"role"` and `"content"`.

Start each session with a system message (a constant or small string) that sets behavior (tone, role, safety).

**3) Persistence (JSON)**

Save history to disk so a later run can continue.

- Load on startup if the file exists; otherwise start fresh (still add the system message)
- Use `json` (readable on disk) and `with open(...)`
- Use `try`/`except` for a missing or bad file

**4) Four actions**

Provide at least four user actions (commands and/or a small menu). Include all of these:

- **Chat** (default: a normal user message → model reply)
- **Clear session** (clear history, keep the program running, restore the system message)
- **Save now** (not only on exit)
- **Quit** (save before exit)

When the program starts, clearly tell the user how to use these actions (show a menu or print the available commands).

Additional commands such as `/help`, `/switch`, `/export`, `/transcript`, `/undo`, and `/redo` count as extensions.

**5) Validation**

- No crashes on bad input
- Reprompt until valid where you ask for choices
- Reject empty messages after `strip()`

**6) Thin program entry loop**

A `main()` function is not required.

Whether you use `main()` or not, your entry loop should mostly wire: load → loop → save on exit.

Heavy work should be in named functions (or class methods), not in a giant top-level loop.

#### Required functions (minimum)

Each action should invoke a function after handling basic input/output.

Core functions for each action must **not** perform input/output themselves. They should only handle logic. Examples:

- `add_message_to_history(history, message)`
- `clear_history(history)`
- `save_history(history, filename)`
- `load_history(filename)`
- `chat(history)` (the starter model call)

Separately, you may write I/O helpers such as:

- `prompt_user_message()`
- `print_menu()`
- `print_reply(reply)`
- `print_error(message)`
- `get_user_action()`

Keep user input and printing out of your core logic functions.

---

## 📤 Submission Instructions

1. Accept the GitHub assignment and create your repo.
2. Set the Python interpreter to **3.12.1**, then run the starter and extend `main.py`.
3. Commit and push your work to GitHub.
4. Copy your GitHub repository URL.
5. Submit the repository URL in Blackboard.

---

## ✅ Submission Checklist

- ☐ Loop runs until quit; save behavior matches your documented rule
- ☐ History is a list of dicts with `role` and `content`; system message is documented
- ☐ JSON load/save uses `with open` and `try`/`except` for a bad or missing file
- ☐ Four actions: chat, clear, save, quit
- ☐ Empty input rejected; invalid choices reprompted
- ☐ Entry loop is thin; logic lives in functions or a small class
- ☐ If aiming for above 90%, extra features listed as `Additional requirements:` in `main.py` and in the Blackboard submission
- ☐ Correct file name (`main.py`)
- ☐ AI Disclaimer included
- ☐ Code follows PEP 8 conventions
- ☐ Code tested with multiple inputs
- ☐ Repository pushed to GitHub
- ☐ Repository URL submitted in Blackboard
