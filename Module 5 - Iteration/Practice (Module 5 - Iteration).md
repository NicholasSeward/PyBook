# Practice Assignment: Module 5 - Iteration

## Overview
Complete **3 problems total** - choose **1 from each section** below. Each section focuses on different aspects of iteration and loops.

## Instructions
- Choose **1 problem from Section 1** (For Loops and range())
- Choose **1 problem from Section 2** (While Loops)  
- Choose **1 problem from Section 3** (Loop Control)
- Use proper PEP 8 coding conventions
- Test your code with different inputs

## File Naming and Submission

### File Naming
Each problem should be a separate file:
- **Problem 1a:** `program1a.py` (Number Pattern Generator)
- **Problem 1b:** `program1b.py` (Multiplication Table)
- **Problem 2a:** `program2a.py` (Guessing Game)
- **Problem 2b:** `program2b.py` (Sum Calculator)
- **Problem 3a:** `program3a.py` (Prime Number Finder)
- **Problem 3b:** `program3b.py` (Menu System)

### AI Disclaimer Requirement
**CRITICAL:** Each file must include an AI Disclaimer at the top. The autograder will look for this exact text and check the content after it.

**Examples of AI Disclaimers (choose the most appropriate or write your own):**

**No AI Use:**
```python
# AI Disclaimer: This code was written without the use of AI tools.
# Any assistance received was from course materials, textbooks, or instructor guidance only.
```

**Minimal AI Use (e.g., syntax help, debugging):**
```python
# AI Disclaimer: This code was written with minimal AI assistance.
# Used AI for: syntax checking and debugging only.
# Core logic and problem-solving approach are my own work.
```

**Moderate AI Use (e.g., code structure, algorithm suggestions):**
```python
# AI Disclaimer: This code was written with moderate AI assistance.
# Used AI for: code structure suggestions and algorithm guidance.
# I implemented the solutions and modified the AI suggestions to fit the requirements.
```

**Extensive AI Use (e.g., significant code generation):**
```python
# AI Disclaimer: This code was written with extensive AI assistance.
# Used AI for: code generation, debugging, and optimization.
# I reviewed, tested, and modified all AI-generated code to ensure it meets requirements.
```

**Unacceptable AI Use (e.g., "vibe coding" without learning):**
```python
# AI Disclaimer: This code was written with extensive AI assistance.
# Used AI for: complete code generation to pass autograder.
# I copied the code without understanding it, just to get a green checkmark.
# I didn't actually learn anything from this assignment.
```

**Your program code starts here...**

### Submission Process
1. Create your program files
2. Test with autograde.py
3. Commit and push to GitHub
4. Verify GitHub Actions shows green checkmark ✅
5. Submit your repository URL

**Example repository URL:** `https://github.com/Seward-Classes/practice-05-username`

---

## Section 1: For Loops and range() (Choose 1)

### Problem 1a: Number Pattern Generator

Create a program that generates number patterns using for loops and range().

**Requirements:**
- Ask the user for a positive integer
- Use for loops and range() to generate patterns
- Display multiple patterns using the same input number
- Use different range() parameters for variety

**Patterns to Generate:**
- Count up from 1 to n
- Count down from n to 1
- Even numbers from 2 to n (if n is even)
- Odd numbers from 1 to n (if n is odd)

**Sample Output:**
```
Enter a positive integer: 6
==========================================
NUMBER PATTERN GENERATOR
==========================================
Input number: 6

Pattern 1 - Count up: 1 2 3 4 5 6
Pattern 2 - Count down: 6 5 4 3 2 1
Pattern 3 - Even numbers: 2 4 6
Pattern 4 - Odd numbers: 1 3 5
==========================================
```

---

### Problem 1b: Multiplication Table

Create a program that generates a multiplication table using for loops and range().

**Requirements:**
- Ask the user for a number (1-12)
- Use nested for loops to generate a multiplication table
- Display the table in a formatted grid
- Use range() to control the loop iterations

**Sample Output:**
```
Enter a number (1-12): 5
==========================================
MULTIPLICATION TABLE FOR 5
==========================================
5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
5 x 4 = 20
5 x 5 = 25
5 x 6 = 30
5 x 7 = 35
5 x 8 = 40
5 x 9 = 45
5 x 10 = 50
==========================================
```

---

## Section 2: While Loops (Choose 1)

### Problem 2a: Guessing Game

Create a program that implements a number guessing game using while loops.

**Requirements:**
- Generate a random number between 1 and 100
- Use a while loop to keep asking for guesses
- Provide hints (too high/too low)
- Count the number of attempts
- End the loop when the correct number is guessed

**Sample Output:**
```
==========================================
NUMBER GUESSING GAME
==========================================
I'm thinking of a number between 1 and 100.
Enter your guess: 50
Too high! Try again.
Enter your guess: 25
Too low! Try again.
Enter your guess: 37
Too high! Try again.
Enter your guess: 31
Congratulations! You guessed it in 4 attempts.
==========================================
```

---

### Problem 2b: Sum Calculator

Create a program that calculates the sum of numbers entered by the user using while loops.

**Requirements:**
- Use a while loop to continuously ask for numbers
- Allow the user to enter numbers until they type 'done'
- Keep a running total of all entered numbers
- Display the final sum and count of numbers entered
- Handle invalid input gracefully

**Sample Output:**
```
==========================================
SUM CALCULATOR
==========================================
Enter a number (or 'done' to finish): 10
Enter a number (or 'done' to finish): 20
Enter a number (or 'done' to finish): 30
Enter a number (or 'done' to finish): done
==========================================
Numbers entered: 3
Total sum: 60
Average: 20.0
==========================================
```

---

## Section 3: Loop Control (Choose 1)

### Problem 3a: Prime Number Finder

Create a program that finds prime numbers using loop control statements.

**Requirements:**
- Ask the user for a positive integer
- Use for loops with break statements to check for prime numbers
- Use continue statements to skip non-prime numbers
- Display all prime numbers from 2 to the given number
- Use efficient prime checking algorithm

**Sample Output:**
```
Enter a positive integer: 20
==========================================
PRIME NUMBER FINDER
==========================================
Prime numbers from 2 to 20:
2 3 5 7 11 13 17 19
Total primes found: 8
==========================================
```

---

### Problem 3b: Menu System

Create a program that implements a menu system using loop control statements.

**Requirements:**
- Display a menu with multiple options
- Use a while loop to keep the menu running
- Use break statements to exit the program
- Use continue statements to restart the menu
- Handle invalid menu choices gracefully
- Implement at least 3 different menu options

**Sample Output:**
```
==========================================
MENU SYSTEM
==========================================
1. Display current time
2. Calculate square of a number
3. Exit
Enter your choice (1-3): 1
Current time: 14:30:25
Press Enter to continue...

==========================================
MENU SYSTEM
==========================================
1. Display current time
2. Calculate square of a number
3. Exit
Enter your choice (1-3): 2
Enter a number: 5
Square of 5 is: 25
Press Enter to continue...

==========================================
MENU SYSTEM
==========================================
1. Display current time
2. Calculate square of a number
3. Exit
Enter your choice (1-3): 3
Goodbye!
==========================================
```

---

## Submission Checklist

- [ ] Completed 1 problem from Section 1 (For Loops and range())
- [ ] Completed 1 problem from Section 2 (While Loops)
- [ ] Completed 1 problem from Section 3 (Loop Control)
- [ ] Each file follows the naming convention
- [ ] Each file includes proper AI disclaimer
- [ ] Each file uses appropriate concepts for its section
- [ ] Each file passes the autograde.py test locally
- [ ] All files are committed and pushed to GitHub
- [ ] GitHub Actions tab shows green checkmark ✅
- [ ] Repository URL is submitted on BlackBoard
---
