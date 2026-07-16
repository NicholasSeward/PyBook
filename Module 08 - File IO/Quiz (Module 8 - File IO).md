# Quiz (Module 8 - File IO)

## Multiple Choice Questions (10 questions)

1. What is the difference between ephemeral and persistent programs?
   a) Ephemeral programs run forever, persistent programs run briefly
   b) Ephemeral programs lose data when they end, persistent programs keep data
   c) Ephemeral programs are faster, persistent programs are slower
   d) Ephemeral programs use databases, persistent programs use files

2. What is the correct way to open a file for reading in Python?
   a) `open('file.txt', 'r')`
   b) `open('file.txt', 'read')`
   c) `open('file.txt', 'w')`
   d) `open('file.txt', 'a')`

3. What happens when you open a file that doesn't exist in write mode?
   a) An error occurs
   b) A new file is created
   c) The program crashes
   d) Nothing happens

4. What is the purpose of the `with` statement when working with files?
   a) To make files read-only
   b) To automatically close files when done
   c) To make files write-only
   d) To encrypt files

5. What is the output of the following code?
   ```python
   with open('test.txt', 'w') as f:
       f.write('Hello')
   ```
   a) Nothing is printed
   b) 'Hello' is printed
   c) The file is created with 'Hello' in it
   d) Error

6. What is the purpose of the `strip()` method when reading files?
   a) To remove whitespace characters from the beginning and end
   b) To add whitespace characters
   c) To split the string into parts
   d) To convert to uppercase

7. What is the correct way to read a file line by line in Python?
   a) `for line in open('filename.txt'):`
   b) `for line in read('filename.txt'):`
   c) `for line in file('filename.txt'):`
   d) `for line in load('filename.txt'):`

8. What is the purpose of the `try-except` block in file handling?
   a) To make files read faster
   b) To handle errors gracefully
   c) To encrypt files
   d) To compress files

9. What is the output of `open('file.txt', 'a')`?
   a) Opens file for reading
   b) Opens file for writing (overwrites)
   c) Opens file for appending
   d) Opens file for reading and writing

10. What is the purpose of the `pickle` module?
    a) To compress files
    b) To serialize Python objects
    c) To encrypt files
    d) To format text files

## Matching Questions (2 questions)

**Question 11:** Match each file mode with its purpose.

| Mode | Purpose |
|------|---------|
| A) `'r'` | 1) Write mode (overwrites) |
| B) `'w'` | 2) Read mode |
| C) `'a'` | 3) Append mode |
| D) `'r+'` | 4) Read and write mode |

**Question 12:** Match each file method with its purpose.

| Method | Purpose |
|--------|---------|
| A) `read()` | 1) Read entire file as string |
| B) `readline()` | 2) Read one line |
| C) `readlines()` | 3) Read all lines as list |
| D) `write()` | 4) Write string to file |

## True/False Questions (3 questions)

13. The `with` statement automatically closes files when you're done with them. (True/False)

14. You can only read from files opened in read mode. (True/False)

15. The `pickle` module can serialize any Python object. (True/False)

## Fill in the Blank Questions (5 questions)

16. The `_____` statement automatically closes files when you're done with them.

17. The `_____` mode opens a file for appending data to the end.

18. The `_____` method reads the entire file as a single string.

19. The `_____` method removes whitespace from the beginning and end of a string.

20. The `_____` module is used to serialize Python objects to files.
