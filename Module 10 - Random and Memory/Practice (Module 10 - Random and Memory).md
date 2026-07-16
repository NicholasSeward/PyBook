# Practice Assignment: Module 10 - Random and Memory

## Overview
Complete **2 problems total** - choose **1 from each section** below. Each section focuses on different aspects of randomization and performance analysis in Python.

## Instructions
- Choose **1 problem from Section 1** (Random Number Generation)
- Choose **1 problem from Section 2** (Timing and Performance)
- Use proper PEP 8 coding conventions
- Test your code with different inputs

## File Naming and Submission

### File Naming
Each problem should be a separate file:
- **Problem 1a:** `program1a.py` (Random Password Generator)
- **Problem 1b:** `program1b.py` (Card Shuffler)
- **Problem 2a:** `program2a.py` (Typewriter Effect)
- **Problem 2b:** `program2b.py` (Gregory-Leibniz Pi Calculation)

### AI Disclaimer
Each file must include an AI Disclaimer at the top.

### Submission Process
1. Create your program files
2. Test your code thoroughly
3. Commit and push to GitHub
4. Submit your repository URL

**Example repository URL:** `https://github.com/Seward-Classes/practice-10-username`

---

## Section 1: Random Number Generation (Choose 1)

### 1a: Random Password Generator

**File:** `program1a.py`

Create a password generator that creates random passwords with customizable options.

**Requirements:**
- Write a function that generates a random password of a given length
- Allow options to include/exclude numbers and symbols
- Use `random.choice()` to select random characters
- Generate and display 3 different passwords with different settings

---

### 1b: Card Shuffler

**File:** `program1b.py`

Simulate a deck of cards and shuffle it using the random module.

**Requirements:**
- Create a standard 52-card deck (13 ranks × 4 suits)
- Use `random.shuffle()` to shuffle the deck
- Deal 5 cards to 2 players
- Display each player's hand
- Use `random.seed()` to make the shuffle reproducible

---

## Section 2: Timing and Performance (Choose 1)

### 2a: Typewriter Effect

**File:** `program2a.py`

Create a typewriter effect that prints characters one at a time with timing.

**Requirements:**
- Write a function that takes a string and prints each character one at a time with a small pause (e.g., `time.sleep(0.05)`) between each character.
  - Hint: Use `print(char, end="")` so the output stays on the same line.
- Allow the user to type in a message (`input()`).
- Use your function to print out the user's message in typewriter style.
- Use `time.perf_counter()` to measure the total time taken to type out the whole string.
- After the function finishes, print out the elapsed time in seconds.

---

### 2b: Gregory-Leibniz Pi Calculation

**File:** `program2b.py`

Calculate pi using the Gregory-Leibniz series.

**Requirements:**
- Write a function that takes in `n` (the number of terms) and returns an approximation of pi using the Gregory-Leibniz series:
  - Formula: pi = 4/1 - 4/3 + 4/5 - 4/7 + 4/9 - ...)
- Ask the user to input how many terms to use.
- Call your function with the user's input, report the calculated value of pi.
- Use `time.perf_counter()` to measure how long the calculation takes.
- After showing the result, leave a comment in your code about:
  - How large `n` needs to be to get the first 5 digits (3.1415) of pi correct,
  - And how long that calculation took on your machine.

---

## Submission Checklist

- [ ] Completed 1 problem from Section 1 (Random Number Generation)
- [ ] Completed 1 problem from Section 2 (Timing and Performance)
- [ ] Each file follows the naming convention (program1a.py, program2a.py, etc.)
- [ ] Each file includes an AI Disclaimer at the top
- [ ] Code is tested and working properly
- [ ] All files are committed and pushed to GitHub
- [ ] Repository URL is submitted on BlackBoard
