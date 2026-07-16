# Practice Assignment: Module 11 - Python Tricks

## Section 1: Overview + Instructions

Complete **any 3 challenges** from Section 2 below. Each challenge focuses on specific “Python tricks” we covered in Module 11.

**Rules:**
- Use proper PEP 8 coding conventions
- Your program must not crash on bad input (use validation / try-except where appropriate)
- You may use helper functions as needed

## GitHub Classroom Link (Get Started)

Accept the assignment here:

👉 **[INSERT GITHUB CLASSROOM LINK HERE]**

## File Naming and Submission

### File Naming

- Each challenge should be a separate file.
- Use this naming rule: **Challenge N → `programN.py`**
  - Example: If you do Challenge 4, submit `program4.py`

### AI Disclaimer Requirement

**CRITICAL:** Each file must include an AI Disclaimer at the top. The autograder will look for this exact text and check the content after it.

Use one of these (copy/paste exactly):

```py
# AI Disclaimer: This code was written without the use of AI tools.
# Any assistance received was from course materials, textbooks, or instructor guidance only.
```

```py
# AI Disclaimer: AI tools were used to help generate ideas and/or debug this code.
# All final code was reviewed, tested, and fully understood by me.
```

### Submission Process

- Create your 3 program files (for the 3 challenges you chose)
- Test your code thoroughly
- Commit and push to GitHub
- Submit your repository URL

---

## Section 2: Challenges (Pick Any 3)

### 1) Dedup + Fast Membership + Stable Output

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

---

### 2) Filter + Map Without Loops

**Required tricks:** list comprehension, optional: f-strings

Write a program that:
- Asks the user to input 5 numbers, one at a time, using a list comprehension (`int(input(f"num{i+1}: "))` as a hint).
- Creates and prints:
  - A list of squares of the **even** numbers
  - A list of the numbers that are **multiples of 3**
  - A list of strings like `"17 -> odd"` or `"20 -> even"` for every number

**Must-haves:**
- Use **at least 3** list comprehensions (including the initial input step)

---

### 3) Build an Index (Enumerate + Dict Comprehension)

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

---

### 4) Pair Up Two Lists (Zip + Sorting with lambda)

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

---

### 5) Password Rules Checker (any/all + Generator Expressions)

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
- Print a short reason when it fails (example: “Missing digit”)

---

### 6) Frequency Report (Counter + f-string formatting)

**Required tricks:** `collections.Counter`, f-strings with format specs

Write a program that:
- Uses this text (hardcode it in your file as a triple-quoted string):
  - Choose a chapter from a public domain book. Here are two options:
    - **Option 1:** Chapter 1 of "Pride and Prejudice" by Jane Austen ([Gutenberg Link](https://www.gutenberg.org/files/1342/1342-h/1342-h.htm#chap01))
    - **Option 2:** Chapter 1 of "The Adventures of Sherlock Holmes" by Arthur Conan Doyle ([Gutenberg Link](https://www.gutenberg.org/files/1661/1661-h/1661-h.htm#chap01))
  - You may pick and copy the text from one of these sources, or another public domain book of your choice. (Project Gutenberg is a great resource: [https://www.gutenberg.org/](https://www.gutenberg.org/))
- Counts the frequency of each word (case-insensitive)
- Prints:
  - The 10 most common words (or fewer if there aren’t 10)
  - Each line should be nicely formatted with aligned columns, like:
    - `word: count`

**Must-haves:**
- Use `Counter(...)`
- Use an f-string format spec to line up output (example: fixed width for the word column)

---

### 7) Grouping Tool (defaultdict + Slicing, with user input)

**Required tricks:** `collections.defaultdict(list)`, slicing

Write a program that:
- Asks the user to enter category/item pairs (example: `fruit apple`), one per line.
- End input by typing `done`.
- Groups items by category into a dictionary like:
  - `{"fruit": ["apple", "banana"], "veg": ["carrot"]}`
- For each category, print:
  - the category name, the number of items, and the list of items.
  - If there are more than 3 items in a category, show only the first 3 items followed by `...`.
  - **Example output:**
    ```
    fruit (3): apple, banana, orange
    veg (2): carrot, spinach
    snacks (5): chips, cookies, popcorn, ...
    ```

**Must-haves:**
- Use `defaultdict(list)` to build the groups
- Use slicing (like `items[:2]`) in your output

---

## Submission Checklist

- [ ] I completed **any 3** challenges from Section 2
- [ ] I used the required Python tricks for each chosen challenge
- [ ] I named files `programN.py` matching the challenge number(s)
- [ ] Each file includes the AI Disclaimer at the top
- [ ] Code is tested and works without crashing
- [ ] All files are committed and pushed to GitHub
- [ ] I submitted my repository URL on Blackboard

