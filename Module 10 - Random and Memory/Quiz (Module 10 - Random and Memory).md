# Quiz (Module 10 - Random and Memory)

## Multiple Choice Questions (10 questions)

1. What is aliasing in Python?
   a) When multiple variables point to the same object in memory
   b) When variables have similar names
   c) When variables are in the same scope
   d) When variables are declared in the same line

2. What is the difference between a shallow copy and a deep copy?
   a) A shallow copy is faster, a deep copy is slower
   b) A shallow copy doesn't copy nested objects, a deep copy does
   c) A shallow copy copies nested objects, a deep copy doesn't
   d) There is no difference

3. What is the output of `random.randint(1, 10)`?
   a) A random integer between 1 and 10, inclusive
   b) A random integer between 1 and 9
   c) A random float between 1 and 10
   d) Always 5

4. What is the purpose of the `random.seed()` function?
   a) To make random numbers truly random
   b) To set a starting point for the random number generator
   c) To stop the random number generator
   d) To make random numbers faster

5. What is the output of `random.choice([1, 2, 3, 4, 5])`?
   a) A random number from the list
   b) The first number in the list
   c) The last number in the list
   d) The sum of all numbers

6. What is the time complexity of linear search?
   a) O(1)
   b) O(log n)
   c) O(n)
   d) O(n²)

7. What is the time complexity of binary search?
   a) O(1)
   b) O(log n)
   c) O(n)
   d) O(n²)

8. What is the output of `time.time()`?
   a) The current time as a string
   b) The current time as a datetime object
   c) The number of seconds since the epoch
   d) The current date

9. What is the purpose of the `time.sleep()` function?
   a) To make the program run faster
   b) To pause the program for a specified number of seconds
   c) To measure how long something takes
   d) To get the current time

10. What is the output of `copy.deepcopy([1, [2, 3]])`?
    a) `[1, [2, 3]]`
    b) `[1, [2, 3]]` (but with independent nested objects)
    c) `[1, 2, 3]`
    d) Error

## Matching Questions (2 questions)

**Question 11:** Match each algorithm with its time complexity.

| Algorithm | Time Complexity |
|-----------|----------------|
| A) Linear search | 1) O(log n) |
| B) Binary search | 2) O(n) |
| C) Bubble sort | 3) O(n²) |
| D) Constant time | 4) O(1) |

**Question 12:** Match each random function with its purpose.

| Function | Purpose |
|----------|---------|
| A) `random.random()` | 1) Random integer in range |
| B) `random.randint()` | 2) Random float between 0 and 1 |
| C) `random.choice()` | 3) Random element from sequence |
| D) `random.shuffle()` | 4) Randomly reorder sequence |

## True/False Questions (3 questions)

13. Pseudorandom numbers are truly random. (True/False)

14. A deep copy creates completely independent copies of nested objects. (True/False)

15. Binary search can only be used on sorted lists. (True/False)

## Fill in the Blank Questions (5 questions)

16. The `_____` function generates a random float between 0.0 and 1.0.

17. A `_____` copy creates a new object but references the same nested objects.

18. The `_____` function pauses the program for a specified number of seconds.

19. `_____` search checks each element in a list until the target is found.

20. The `_____` function sets a starting point for the random number generator.

## Answer Key

**Multiple Choice:**
1. a) When multiple variables point to the same object in memory
2. b) A shallow copy doesn't copy nested objects, a deep copy does
3. a) A random integer between 1 and 10, inclusive
4. b) To set a starting point for the random number generator
5. a) A random number from the list
6. c) O(n)
7. b) O(log n)
8. c) The number of seconds since the epoch
9. b) To pause the program for a specified number of seconds
10. b) `[1, [2, 3]]` (but with independent nested objects)

**Matching:**
11. A-2, B-1, C-3, D-4
12. A-2, B-1, C-3, D-4

**True/False:**
13. False
14. True
15. True

**Fill in the Blank:**
16. `random.random()`
17. `shallow`
18. `time.sleep()`
19. `linear`
20. `random.seed()`
