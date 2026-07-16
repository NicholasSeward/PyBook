# Quiz (Module 11 - Python Tricks)

## Multiple Choice Questions (10 questions)

1. What is a set in Python?
   a) A collection of unique elements
   b) A collection of ordered elements
   c) A collection of key-value pairs
   d) A collection of functions

2. What is the main advantage of using sets for membership testing?
   a) Sets are always sorted
   b) Sets use O(1) time for membership testing
   c) Sets can contain any type of data
   d) Sets are easier to create

3. What is a list comprehension?
   a) A way to create lists using a concise syntax
   b) A way to sort lists
   c) A way to merge lists
   d) A way to delete lists

4. What is the output of `[x**2 for x in range(5)]`?
   a) `[0, 1, 4, 9, 16]`
   b) `[1, 4, 9, 16, 25]`
   c) `[0, 1, 2, 3, 4]`
   d) `[2, 4, 6, 8, 10]`

5. What is a conditional expression (ternary operator)?
   a) A way to write if-else statements in one line
   b) A way to create loops
   c) A way to define functions
   d) A way to import modules

6. What is the output of `x = 5 if True else 10`?
   a) `5`
   b) `10`
   c) `True`
   d) Error

7. What is an iterator in Python?
   a) A function that returns multiple values
   b) An object that can be iterated over
   c) A type of loop
   d) A collection of data

8. What is a generator function?
   a) A function that creates other functions
   b) A function that yields values one at a time
   c) A function that returns a list
   d) A function that modifies global variables

9. What is the purpose of the `lambda` keyword?
   a) To create anonymous functions
   b) To create classes
   c) To create modules
   d) To create loops

10. What is the output of `list(zip([1, 2], ['a', 'b']))`?
    a) `[1, 2, 'a', 'b']`
    b) `[(1, 'a'), (2, 'b')]`
    c) `[1, 'a', 2, 'b']`
    d) Error

## Matching Questions (2 questions)

**Question 11:** Match each Python feature with its description.

| Feature | Description |
|---------|-------------|
| A) Set | 1) Collection of unique elements |
| B) List comprehension | 2) Concise way to create lists |
| C) Lambda function | 3) Anonymous function |
| D) Generator | 4) Function that yields values |

**Question 12:** Match each function with its purpose.

| Function | Purpose |
|----------|---------|
| A) `map()` | 1) Apply function to each item |
| B) `filter()` | 2) Keep items that meet condition |
| C) `zip()` | 3) Combine multiple sequences |
| D) `enumerate()` | 4) Get index and value pairs |

## True/False Questions (3 questions)

13. Sets in Python maintain the order of their elements. (True/False)

14. List comprehensions are always faster than equivalent for loops. (True/False)

15. Lambda functions can contain multiple statements. (True/False)

## Fill in the Blank Questions (5 questions)

16. Fill in the blank to remove duplicates from a list:
```python
numbers = [1, 2, 2, 3, 3, 4]
unique_numbers = _____(_______)
```

17. Fill in the blank to create a list of squares using a list comprehension:
```python
squares = [_____ for x in range(5)]
```

18. Fill in the blank to create a lambda function that doubles a number:
```python
double = _____ x: x * 2
```

19. Fill in the blank to convert all strings to uppercase using map():
```python
words = ['hello', 'world']
uppercase = list(_____(lambda s: s.upper(), words))
```

20. Fill in the blank to combine two lists into pairs:
```python
names = ['Alice', 'Bob']
ages = [25, 30]
pairs = list(_____(names, ages))
```

## Answer Key

**Multiple Choice:**
1. a) A collection of unique elements
2. b) Sets use O(1) time for membership testing
3. a) A way to create lists using a concise syntax
4. a) `[0, 1, 4, 9, 16]`
5. a) A way to write if-else statements in one line
6. a) `5`
7. b) An object that can be iterated over
8. b) A function that yields values one at a time
9. a) To create anonymous functions
10. b) `[(1, 'a'), (2, 'b')]`

**Matching:**
11. A-1, B-2, C-3, D-4
12. A-1, B-2, C-3, D-4

**True/False:**
13. False
14. False
15. False

**Fill in the Blank:**
16. `set(numbers)` or `list(set(numbers))`
17. `x**2` or `x * x`
18. `lambda`
19. `map`
20. `zip`
