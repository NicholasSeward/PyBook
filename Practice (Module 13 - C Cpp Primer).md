# Practice Assignment: Module 13 - C Cpp Primer

## Overview

This assignment provides an opportunity to apply the concepts covered in this module by writing a short C++ program using I/O, loops, and (for one option) randomness.

You will complete:

- One problem total (either Section 1 – Triangle of Stars **or** Section 2 – Hi-Lo Guessing Game)

---

## ▶️ Start Here

Before you begin, watch the walkthrough video below for guidance on how to approach this assignment.

*[Insert walkthrough video about completing programming assignments]*

In GitHub Codespaces, open your `.cpp` file and press **Run** (or Run → Run Without Debugging) to build and run the active C++ file. You do not need bash commands for a first build.

---

## 🚀 GitHub Classroom

Open the GitHub Classroom assignment using the link below.

**GitHub Classroom Assignment**

[INSERT ASSIGNMENT LINK]

> WARNING: Submit the **repository** URL in the LMS (Blackboard), not a Codespaces / `github.dev` link (those are private to you).

---

## 📋 Assignment Requirements

Complete:

- One problem total (Triangle of Stars **or** Hi-Lo Guessing Game)
- Use clear, readable code and standard C++17
- Test your code with multiple inputs
- Include the required AI Disclaimer
- Commit and push your work to GitHub
- Submit your GitHub repository URL in Blackboard

---

## 📁 File Naming

Save your chosen problem as a separate C++ file.

| Problem | File Name |
|---------|-----------|
| Triangle of Stars | `program1a.cpp` |
| Hi-Lo Guessing Game | `program2a.cpp` |

---

## 🤖 AI Usage Disclosure

**CRITICAL:** Each C++ file must begin with an AI Disclaimer. The autograder will look for this exact text and check the content after it.

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

### Section 1 - Basics and I/O (Choose One)

#### Problem 1a: Triangle of Stars

Write a program that asks for a positive integer `n` and prints a left-aligned triangle of `*` of height `n`.

**Requirements:**

- Prompt the user: `Enter a positive integer: ` and read `n`
- If `n <= 0`, you may print an error and exit (optional)
- Print `n` lines; line i contains i stars

**Sample Output:**

```text
Enter a positive integer: 4
*
**
***
****
```

**Starter shape:**

```cpp
#include <iostream>

int main() {
    std::cout << "Enter a positive integer: ";
    int n{};
    std::cin >> n;

    // TODO: Validate n > 0 (optional)

    // TODO: Print a left-aligned triangle of height n.
    // Hint: Use two nested for-loops:
    //   - outer loop controls the number of rows (1..n)
    //   - inner loop prints the right number of '*' for that row

    return 0;
}
```

---

### Section 2 - Randomness and Control Flow (Choose One)

#### Problem 2a: Hi-Lo Guessing Game (Mersenne Twister)

The program picks a secret number in [1, 100]. After each user guess, print `Too low`, `Too high`, or `You got it!`. Continue until correct.

**Requirements:**

- Use `std::random_device`, `std::mt19937`, and `std::uniform_int_distribution<int>` to generate the secret
- Prompt for guesses in a loop
- Validate input is an integer; if not, clear and retry
- End when the user guesses correctly

**Sample Output:**

```text
I'm thinking of a number between 1 and 100. Try to guess it!
Enter your guess: 20
Too low
Enter your guess: 90
Too high
Enter your guess: 65
You got it!
```

**Starter shape:**

```cpp
#include <iostream>
#include <random>

int main() {
    // Generate secret number in [1, 100]
    std::random_device rd;
    std::mt19937 gen(rd());
    std::uniform_int_distribution<int> dist(1, 100);
    int secret = dist(gen);

    // TODO: Prompt user and play Hi-Lo guessing game
    // - Prompt for guesses in a loop
    // - Validate input is an integer; if not, clear and retry
    // - After each guess, print "Too low", "Too high", or "You got it!"
    // - Continue until the user guesses correctly

    return 0;
}
```

**Hints:**

- Use `if (guess < secret)`, `else if (guess > secret)`, `else`
- To limit attempts, add a counter and break after N tries
- For replay, wrap logic in a loop and regenerate `secret`

---

## 📤 Submission Instructions

1. Complete the required programming problem.
2. Commit and push your files to GitHub.
3. Copy your GitHub repository URL.
4. Submit the repository URL in Blackboard.

---

## ✅ Submission Checklist

- ☐ Completed one problem (Triangle **or** Hi-Lo)
- ☐ Correct file name (`program1a.cpp` or `program2a.cpp`)
- ☐ AI Disclaimer included
- ☐ Code follows clear C++17 style
- ☐ Code tested with multiple inputs
- ☐ Repository pushed to GitHub
- ☐ Repository URL submitted in Blackboard
