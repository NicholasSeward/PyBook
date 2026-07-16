# Quiz (Module 6 - Data Structures)

## Multiple Choice Questions (10 questions)

1. What is the correct way to create an empty list in Python?
   a) `list = []`
   b) `list = ()`
   c) `list = {}`
   d) `list = None`

2. Which of the following is a mutable data type in Python?
   a) String
   b) Tuple
   c) List
   d) Integer

3. What is the output of the following code?
   ```python
   numbers = [1, 2, 3, 4, 5]
   numbers[2] = 10
   print(numbers)
   ```
   a) `[1, 2, 10, 4, 5]`
   b) `[1, 2, 3, 4, 5]`
   c) Error
   d) `[1, 2, 3, 10, 4, 5]`

4. What method is used to add an item to the end of a list?
   a) `add()`
   b) `append()`
   c) `insert()`
   d) `extend()`

5. What is the output of `len([1, 2, 3])`?
   a) 3
   b) 2
   c) 1
   d) Error

6. What is the purpose of the `in` operator with lists?
   a) To add items to a list
   b) To check if an item exists in a list
   c) To remove items from a list
   d) To sort a list

7. What is the output of the following code?
   ```python
   my_dict = {'a': 1, 'b': 2}
   print(my_dict['a'])
   ```
   a) `'a'`
   b) `1`
   c) `2`
   d) Error

8. What method is used to get a value from a dictionary with a default if the key doesn't exist?
   a) `get()`
   b) `find()`
   c) `search()`
   d) `lookup()`

9. What is the output of `(1, 2, 3)[1]`?
   a) `1`
   b) `2`
   c) `3`
   d) Error

10. What is the purpose of the `keys()` method for dictionaries?
    a) To get all the values
    b) To get all the keys
    c) To get all the key-value pairs
    d) To add new keys

## Matching Questions (2 questions)

**Question 11:** Match each data structure with its characteristic.

| Data Structure | Characteristic |
|----------------|----------------|
| A) List | 1) Ordered, immutable collection |
| B) Tuple | 2) Ordered, mutable collection |
| C) Dictionary | 3) Unordered, key-value pairs |
| D) Set | 4) Unordered, unique elements |

**Question 12:** Match each list method with its purpose.

| Method | Purpose |
|--------|---------|
| A) `append()` | 1) Add item at specific position |
| B) `insert()` | 2) Add item at the end |
| C) `remove()` | 3) Remove first occurrence of item |
| D) `pop()` | 4) Remove and return item at index |

## True/False Questions (3 questions)

13. Lists in Python can contain elements of different types. (True/False)

14. Dictionaries maintain the order of their key-value pairs in all Python versions. (True/False)

15. Tuples are faster than lists for iteration. (True/False)

## Fill in the Blank Questions (5 questions)

16. A `_____` is an ordered, mutable collection of items.

17. A `_____` is an unordered collection of key-value pairs.

18. The `_____` method adds an item to the end of a list.

19. A `_____` is an ordered, immutable collection of items.

20. The `_____` method removes and returns an item from a list at a specific index.

## Answer Key

**Multiple Choice:**
1. a) `list = []`
2. c) List
3. a) `[1, 2, 10, 4, 5]`
4. b) `append()`
5. a) 3
6. b) To check if an item exists in a list
7. b) `1`
8. a) `get()`
9. b) `2`
10. b) To get all the keys

**Matching:**
11. A-2, B-1, C-3, D-4
12. A-2, B-1, C-3, D-4

**True/False:**
13. True
14. False
15. True

**Fill in the Blank:**
16. `list`
17. `dictionary`
18. `append()`
19. `tuple`
20. `pop()`
