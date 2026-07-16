# Practice Assignment: Module 7 - String Manipulation

## Overview
Complete **3 problems total** - choose **1 from each section** below. Each section focuses on different aspects of string manipulation in Python.

## Instructions
- Choose **1 problem from Section 1** (String Slicing and Methods)
- Choose **1 problem from Section 2** (Text Processing and Pattern Matching)  
- Choose **1 problem from Section 3** (Advanced String Operations)
- Use proper PEP 8 coding conventions
- Test your code with different inputs

## File Naming and Submission

### File Naming
Each problem should be a separate file:
- **Problem 1a:** `program1a.py` (Text Reverser)
- **Problem 1b:** `program1b.py` (Password Validator)
- **Problem 2a:** `program2a.py` (Email Extractor)
- **Problem 2b:** `program2b.py` (Text Analyzer)
- **Problem 3a:** `program3a.py` (Caesar Cipher)
- **Problem 3b:** `program3b.py` (File Path Parser)

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
2. Test your code thoroughly
3. Commit and push to GitHub
4. Submit your repository URL

**Example repository URL:** `https://github.com/Seward-Classes/practice-07-username`

---

## Section 1: String Slicing and Methods (Choose 1)

### Problem 1a: Text Reverser

Create a program that reverses text in various ways using string slicing and string methods.

**Requirements:**
- Ask the user to enter a sentence
- Reverse the entire string using slicing
- Reverse the order of words (keep each word intact)
- Reverse each word individually (keep word order)
- Use string methods: split(), join(), strip()
- Use string slicing with negative indices
- Display all versions of the reversed text

**Sample Output:**
```
==========================================
TEXT REVERSER
==========================================
Enter a sentence: Hello World Python
==========================================
Original text: Hello World Python
Character reverse: nohtyP dlroW olleH
Word order reverse: Python World Hello
Each word reverse: olleH dlroW nohtyP
==========================================
```

---

### Problem 1b: Password Validator

Create a program that validates passwords using string methods.

**Requirements:**
- Ask the user to enter a password
- Check if password meets all requirements:
  - At least 8 characters long
  - Contains at least one uppercase letter
  - Contains at least one lowercase letter
  - Contains at least one digit
  - Contains at least one special character
- Use string methods: isalpha(), isdigit(), isupper(), islower()
- Provide specific feedback on which requirements are not met
- Display whether password is valid or invalid

**Sample Output:**
```
==========================================
PASSWORD VALIDATOR
==========================================
Enter a password: Pass123!
==========================================
Checking password: Pass123!
Length (8+ chars): ✓ (8 characters)
Uppercase letter: ✓
Lowercase letter: ✓
Digit: ✓
Special character: ✓
==========================================
Password is VALID!
==========================================
```

**Sample Output (Invalid):**
```
==========================================
PASSWORD VALIDATOR
==========================================
Enter a password: pass123
==========================================
Checking password: pass123
Length (8+ chars): ✗ (7 characters)
Uppercase letter: ✗
Lowercase letter: ✓
Digit: ✓
Special character: ✗
==========================================
Password is INVALID!
Requirements not met: Length, Uppercase, Special character
==========================================
```

---

## Section 2: Text Processing and Pattern Matching (Choose 1)

### Problem 2a: Email Extractor

Create a program that extracts and validates email addresses using regular expressions.

**Requirements:**
- Ask the user to enter text containing email addresses
- Use regex to find all email addresses in the text
- Extract username and domain from each email
- Count total emails found
- Display all extracted emails with their components
- Use re.findall() or re.search()
- Handle multiple emails in one text block

**Sample Output:**
```
==========================================
EMAIL EXTRACTOR
==========================================
Enter text containing emails:
Contact john.doe@example.com or jane_smith@company.org for info
==========================================
Emails found: 2

Email 1: john.doe@example.com
  Username: john.doe
  Domain: example.com

Email 2: jane_smith@company.org
  Username: jane_smith
  Domain: company.org
==========================================
```

---

### Problem 2b: Text Analyzer

Create a program that analyzes text using string methods and character operations.

**Requirements:**
- Ask the user to enter a paragraph of text
- Count total characters, words, and sentences
- Count vowels and consonants
- Find the longest word
- Calculate average word length
- Display character frequency for top 5 most common characters
- Use string methods: split(), count(), lower()
- Handle punctuation appropriately

**Sample Output:**
```
==========================================
TEXT ANALYZER
==========================================
Enter text to analyze:
The quick brown fox jumps over the lazy dog.
==========================================
ANALYSIS RESULTS
==========================================
Total characters: 44
Total words: 9
Total sentences: 1
Vowels: 12
Consonants: 24
Longest word: "quick" (5 letters)
Average word length: 3.89

Top 5 most common characters:
  o: 4
  e: 3
  u: 2
  h: 2
  r: 2
==========================================
```

---

## Section 3: Advanced String Operations (Choose 1)

### Problem 3a: Caesar Cipher

Create a program that encrypts and decrypts text using the Caesar cipher with ASCII operations.

**Requirements:**
- Ask the user to choose encrypt or decrypt
- Ask for the text to process
- Ask for the shift value (1-25)
- Use ord() and chr() functions to shift letters
- Keep non-letter characters unchanged
- Preserve uppercase and lowercase
- Handle wrap-around (z+1 = a, Z+1 = A)
- Display the processed text

**Sample Output (Encryption):**
```
==========================================
CAESAR CIPHER
==========================================
1. Encrypt
2. Decrypt
Choose operation: 1

Enter text to encrypt: Hello World!
Enter shift value (1-25): 3
==========================================
Original text: Hello World!
Encrypted text: Khoor Zruog!
Shift value: 3
==========================================
```

**Sample Output (Decryption):**
```
==========================================
CAESAR CIPHER
==========================================
1. Encrypt
2. Decrypt
Choose operation: 2

Enter text to decrypt: Khoor Zruog!
Enter shift value (1-25): 3
==========================================
Encrypted text: Khoor Zruog!
Decrypted text: Hello World!
Shift value: 3
==========================================
```

---

### Problem 3b: File Path Parser

Create a program that parses and manipulates file paths using string operations and escape characters.

**Requirements:**
- Ask the user to enter a file path
- Parse the path to extract:
  - Drive letter (if Windows path)
  - Directory path
  - File name
  - File extension
- Convert between Windows (backslash) and Unix (forward slash) paths
- Handle escape characters properly
- Use string methods: split(), rsplit(), replace()
- Display all components of the path

**Sample Output (Windows Path):**
```
==========================================
FILE PATH PARSER
==========================================
Enter a file path: C:\Users\Documents\report.pdf
==========================================
Original path: C:\Users\Documents\report.pdf

Path components:
  Drive: C:
  Directory: \Users\Documents
  Full filename: report.pdf
  Name: report
  Extension: .pdf

Converted to Unix: C:/Users/Documents/report.pdf
==========================================
```

**Sample Output (Unix Path):**
```
==========================================
FILE PATH PARSER
==========================================
Enter a file path: /home/user/documents/data.txt
==========================================
Original path: /home/user/documents/data.txt

Path components:
  Drive: (none)
  Directory: /home/user/documents
  Full filename: data.txt
  Name: data
  Extension: .txt

Converted to Windows: \home\user\documents\data.txt
==========================================
```

---

## Submission Checklist

- [ ] Completed 1 problem from Section 1 (String Slicing and Methods)
- [ ] Completed 1 problem from Section 2 (Text Processing and Pattern Matching)
- [ ] Completed 1 problem from Section 3 (Advanced String Operations)
- [ ] Each file follows the naming convention
- [ ] Each file includes proper AI disclaimer
- [ ] Each file uses appropriate string manipulation concepts
- [ ] Code is tested and working properly
- [ ] All files are committed and pushed to GitHub
- [ ] Repository URL is submitted on BlackBoard
---

