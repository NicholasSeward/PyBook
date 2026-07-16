# Quiz (Module 5 - Iteration)

## Multiple Choice Questions (10 questions)

1. What is the purpose of an accumulator in programming?
   a) To count how many times something happens
   b) To add up values as you go through a loop
   c) To store the maximum value found
   d) To collect items in a list

2. What is the correct way to initialize a counter variable?
   a) `counter = 1`
   b) `counter = 0`
   c) `counter = []`
   d) `counter = None`

3. What is the output of the following code?
   ```python
   numbers = [1, 2, 3, 4, 5]
   total = 0
   for num in numbers:
       total += num
   print(total)
   ```
   a) 0
   b) 15
   c) 5
   d) Error

4. What is the purpose of the `range()` function?
   a) To create a list of numbers
   b) To create a sequence of numbers for iteration
   c) To find the range of a list
   d) To sort a list

5. What is the output of `range(5)`?
   a) `[0, 1, 2, 3, 4]`
   b) `[1, 2, 3, 4, 5]`
   c) `[0, 1, 2, 3, 4, 5]`
   d) `[1, 2, 3, 4]`

6. What is the purpose of the `enumerate()` function?
   a) To count items in a list
   b) To get both index and value while iterating
   c) To sort a list
   d) To reverse a list

7. What is the output of the following code?
   ```python
   for i in range(3):
       print(i, end=' ')
   ```
   a) `0 1 2`
   b) `1 2 3`
   c) `0 1 2 `
   d) `0, 1, 2`

8. What is the purpose of the `break` statement in a loop?
   a) To skip the current iteration
   b) To exit the loop completely
   c) To continue to the next iteration
   d) To restart the loop

9. What is the purpose of the `continue` statement in a loop?
   a) To skip the current iteration and continue to the next
   b) To exit the loop completely
   c) To restart the loop
   d) To pause the loop

10. What is the output of `len([1, 2, 3])`?
    a) 3
    b) 2
    c) 1
    d) Error

## Matching Questions (2 questions)

**Question 11:** Match each loop control statement with its purpose.

| Statement | Purpose |
|-----------|---------|
| A) `break` | 1) Skip current iteration, continue to next |
| B) `continue` | 2) Exit the loop completely |
| C) `pass` | 3) Do nothing (placeholder) |
| D) `return` | 4) Exit the function |

**Question 12:** Match each iteration method with its description.

| Method | Description |
|--------|-------------|
| A) Index-based iteration | 1) Using `for item in list` |
| B) Direct iteration | 2) Using `for i in range(len(list))` |
| C) Enumerate | 3) Getting both index and value |
| D) While loop | 4) Repeating while a condition is true |

## True/False Questions (3 questions)

13. A `for` loop can iterate over any iterable object in Python. (True/False)

14. The `range()` function creates a list of numbers. (True/False)

15. You can use `break` and `continue` in both `for` and `while` loops. (True/False)

## Fill in the Blank Questions (5 questions)

16. An `_____` is a variable that accumulates values during iteration.

17. The `_____` function creates a sequence of numbers for iteration.

18. A `_____` is a variable that counts how many times something happens.

19. The `_____` statement exits a loop immediately.

20. The `_____` statement skips the current iteration and continues to the next.

## Answer Key

**Multiple Choice:**
1. b) To add up values as you go through a loop
2. b) `counter = 0`
3. b) 15
4. b) To create a sequence of numbers for iteration
5. a) `[0, 1, 2, 3, 4]`
6. b) To get both index and value while iterating
7. c) `0 1 2 `
8. b) To exit the loop completely
9. a) To skip the current iteration and continue to the next
10. a) 3

**Matching:**
11. A-2, B-1, C-3, D-4
12. A-2, B-1, C-3, D-4

**True/False:**
13. True
14. False
15. True

**Fill in the Blank:**
16. `accumulator`
17. `range()`
18. `counter`
19. `break`
20. `continue`
