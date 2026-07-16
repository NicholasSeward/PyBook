# Tutorial (Module 10 - Random and Memory)

## Basic Random Numbers

**Try this code:**

```python
import random

# Generate different types of random numbers
a = random.random()
b = random.randint(1, 10)
c = random.choice(['apple', 'banana', 'cherry'])

print(f"random(): {a}")
print(f"randint(1, 10): {b}")
print(f"choice: {c}")
```

**Question 1:** What type of value does `random.random()` return?
- A) An integer between 0 and 1
- B) A float between 0.0 and 1.0
- C) A random string
- D) A boolean value

**Question 2:** Run the code multiple times. What happens?
- A) You get the exact same output each time
- B) You get different random values each time
- C) The program crashes
- D) You get an error

---

## Random Seeds

**Try this code:**

```python
import random

# First run without seed
random.seed(42)
print(random.randint(1, 100))
print(random.randint(1, 100))
print(random.randint(1, 100))

# Reset with same seed
random.seed(42)
print(random.randint(1, 100))
print(random.randint(1, 100))
print(random.randint(1, 100))
```

**Question 3:** What pattern do you observe in the output?
- A) All numbers are the same
- B) The first three numbers are different from the last three
- C) The first three numbers match the last three numbers
- D) All numbers are completely random

**Question 4:** What happens if you remove the second `random.seed(42)` line?
- A) The last three numbers stay the same
- B) The last three numbers will be different
- C) You get an error
- D) The program doesn't run

---

## Random Choice and Shuffle

**Try this code:**

```python
import random

fruits = ['apple', 'banana', 'cherry', 'date', 'elderberry']

# Pick one random fruit
random_fruit = random.choice(fruits)
print(f"Random choice: {random_fruit}")

# Pick 3 random fruits (without replacement)
sample = random.sample(fruits, 3)
print(f"Sample: {sample}")

# Shuffle the list
random.shuffle(fruits)
print(f"Shuffled: {fruits}")
```

**Question 5:** What does `random.sample(fruits, 3)` return?
- A) One random fruit
- B) A list with 3 random fruits (no duplicates)
- C) A list with 3 random fruits (possible duplicates)
- D) The original list

**Question 6:** What happens to the `fruits` list after calling `random.shuffle(fruits)`?
- A) The original list is unchanged
- B) The original list is reordered in place
- C) A new shuffled list is created
- D) The list is sorted

---

## Understanding Aliasing

**Try this code:**

```python
# Create a list
list1 = [1, 2, 3, 4, 5]
list2 = list1

# Modify through list2
list2[0] = 99

print(f"list1: {list1}")
print(f"list2: {list2}")
print(f"list1 is list2: {list1 is list2}")
```

**Question 7:** What does this code print for `list1`?
- A) `[1, 2, 3, 4, 5]`
- B) `[99, 2, 3, 4, 5]`
- C) `[99]`
- D) Error

**Question 8:** What does `list1 is list2` evaluate to?
- A) `True` - they point to the same object
- B) `False` - they are different objects
- C) `None`
- D) Error

---

## Aliasing with Functions

**Try this code:**

```python
def modify_list(my_list):
    my_list.append(100)
    my_list[0] = 999

original = [1, 2, 3]
modify_list(original)
print(original)
```

**Question 9:** What does this code print?
- A) `[1, 2, 3]` - unchanged
- B) `[999, 2, 3, 100]`
- C) `[1, 2, 3, 100]`
- D) Error

**Question 10:** How would you prevent the function from modifying the original list?
- A) Pass a copy: `modify_list(original.copy())`
- B) Use `original = [1, 2, 3]` again after the function
- C) Add `return my_list` to the function
- D) Use `del my_list` at the end of the function

---

## Shallow Copy

**Try this code:**

```python
import copy

# Original list with nested list
original = [1, 2, [3, 4]]
shallow = copy.copy(original)

# Modify the nested list through shallow copy
shallow[2][0] = 99

print(f"Original: {original}")
print(f"Shallow: {shallow}")
```

**Question 11:** What does this code print for `original`?
- A) `[1, 2, [3, 4]]` - unchanged
- B) `[1, 2, [99, 4]]` - nested list was modified
- C) `[1, 2, 99]`
- D) Error

**Question 12:** What happens if you change `shallow[0] = 77` (modifying a top-level element)?
- A) Both original and shallow change
- B) Only shallow changes
- C) Only original changes
- D) Neither changes

---

## Deep Copy

**Try this code:**

```python
import copy

# Original list with nested list
original = [1, 2, [3, 4]]
deep = copy.deepcopy(original)

# Modify the nested list through deep copy
deep[2][0] = 99
deep[0] = 77

print(f"Original: {original}")
print(f"Deep: {deep}")
```

**Question 13:** What does this code print for `original`?
- A) `[1, 2, [3, 4]]` - completely unchanged
- B) `[77, 2, [99, 4]]` - both changes applied
- C) `[1, 2, [99, 4]]` - only nested change applied
- D) Error

**Question 14:** When should you use `deepcopy()` instead of `copy()`?
- A) When you have nested data structures and need complete independence
- B) When you want to save memory
- C) When you want faster performance
- D) When working with simple integers

---

## List References

**Try this code:**

```python
a = [1, 2, 3]
b = [1, 2, 3]
c = a

print(f"a == b: {a == b}")
print(f"a is b: {a is b}")
print(f"a == c: {a == c}")
print(f"a is c: {a is c}")
```

**Question 15:** What is the difference between `==` and `is` in this context?
- A) `==` checks if values are equal, `is` checks if they're the same object
- B) They do the exact same thing
- C) `is` checks values, `==` checks object identity
- D) There is no difference for lists

**Question 16:** Fill in the blank: The `is` operator checks for _____.
- A) equality
- B) identity
- C) similarity
- D) membership

---

## Measuring Performance

**Try this code:**

```python
import time

# Approach 1: Using a loop
start = time.perf_counter()
result1 = []
for i in range(1000000):
    result1.append(i * 2)
end = time.perf_counter()
time1 = end - start

# Approach 2: Using list comprehension
start = time.perf_counter()
result2 = [i * 2 for i in range(1000000)]
end = time.perf_counter()
time2 = end - start

print(f"Loop time: {time1:.4f} seconds")
print(f"List comprehension time: {time2:.4f} seconds")
print(f"List comprehension is {time1/time2:.2f}x faster")
```

**Question 17:** Which approach is typically faster?
- A) The loop approach
- B) The list comprehension approach
- C) They are exactly the same speed
- D) It varies randomly

**Question 18:** What does `time.perf_counter()` return?
- A) The current date and time
- B) A high-resolution time value in seconds
- C) The number of milliseconds elapsed
- D) The CPU usage percentage

---

## Linear Search Performance

**Try this code:**

```python
import time

def linear_search(lst, target):
    for i in range(len(lst)):
        if lst[i] == target:
            return i
    return -1

# Test with different sized lists
sizes = [1000, 10000, 100000]

for size in sizes:
    test_list = list(range(size))
    
    start = time.perf_counter()
    result = linear_search(test_list, size - 1)  # Search for last item
    end = time.perf_counter()
    
    print(f"Size {size}: {(end - start)*1000:.4f} milliseconds")
```

**Question 19:** What pattern do you observe as the list size increases?
- A) Time stays constant
- B) Time increases proportionally (linear growth)
- C) Time increases exponentially
- D) Time decreases

**Question 20:** Fill in the blank: Linear search has a time complexity of _____.
- A) O(1)
- B) O(log n)
- C) O(n)
- D) O(n²)

---

## Comparing Search Algorithms

**Try this code:**

```python
import time

def linear_search(lst, target):
    for i in range(len(lst)):
        if lst[i] == target:
            return i
    return -1

def binary_search(lst, target):
    left, right = 0, len(lst) - 1
    while left <= right:
        mid = (left + right) // 2
        if lst[mid] == target:
            return mid
        elif lst[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1

# Create a large sorted list
test_list = list(range(1000000))
target = 999999

# Test linear search
start = time.perf_counter()
linear_search(test_list, target)
linear_time = time.perf_counter() - start

# Test binary search
start = time.perf_counter()
binary_search(test_list, target)
binary_time = time.perf_counter() - start

print(f"Linear search: {linear_time:.6f} seconds")
print(f"Binary search: {binary_time:.6f} seconds")
print(f"Binary search is {linear_time/binary_time:.0f}x faster")
```

**Question 21:** Which search algorithm is faster for large sorted lists?
- A) Linear search
- B) Binary search
- C) They are the same speed
- D) It depends on the target value

**Question 22:** What requirement does binary search have that linear search doesn't?
- A) The list must be sorted
- B) The list must contain integers
- C) The list must be small
- D) The list must have unique values

---

## Random Dice Game

**Try this code:**

```python
import random

def roll_dice():
    return random.randint(1, 6)

def play_game():
    player1 = roll_dice() + roll_dice()
    player2 = roll_dice() + roll_dice()
    
    print(f"Player 1 rolled: {player1}")
    print(f"Player 2 rolled: {player2}")
    
    if player1 > player2:
        return "Player 1 wins!"
    elif player2 > player1:
        return "Player 2 wins!"
    else:
        return "It's a tie!"

print(play_game())
```

**Question 23:** What is the range of possible values for each player's total?
- A) 1 to 6
- B) 2 to 12
- C) 0 to 12
- D) 1 to 12

**Question 24:** How would you make the game reproducible (same results each time)?
- A) Add `random.seed(0)` at the beginning
- B) Remove the `random` import
- C) Use `random.choice()` instead
- D) Add a loop

---

## Time Complexity Comparison

**Try this code:**

```python
import time

# O(1) - Constant time
def constant_time(lst):
    return lst[0] if lst else None

# O(n) - Linear time
def linear_time(lst):
    total = 0
    for num in lst:
        total += num
    return total

# O(n²) - Quadratic time
def quadratic_time(lst):
    count = 0
    for i in lst:
        for j in lst:
            count += 1
    return count

# Test with different sizes
for size in [100, 1000, 10000]:
    test_list = list(range(size))
    
    start = time.perf_counter()
    constant_time(test_list)
    t1 = (time.perf_counter() - start) * 1000
    
    start = time.perf_counter()
    linear_time(test_list)
    t2 = (time.perf_counter() - start) * 1000
    
    start = time.perf_counter()
    quadratic_time(test_list)
    t3 = (time.perf_counter() - start) * 1000
    
    print(f"\nSize {size}:")
    print(f"  O(1): {t1:.6f} ms")
    print(f"  O(n): {t2:.6f} ms")
    print(f"  O(n²): {t3:.2f} ms")
```

**Question 25:** What happens to O(n²) time as the input size grows?
- A) It stays constant
- B) It grows slowly
- C) It grows proportionally
- D) It grows very rapidly

**Question 26:** Which complexity is best for large datasets?
- A) O(n²)
- B) O(n)
- C) O(1)
- D) O(2ⁿ)

---

## Understanding `time.sleep()`

**Try this code:**

```python
import time

print("Starting...")
start = time.time()

time.sleep(2)  # Pause for 2 seconds

end = time.time()
elapsed = end - start

print(f"Finished after {elapsed:.2f} seconds")
```

**Question 27:** What does `time.sleep(2)` do?
- A) Pauses the program for 2 seconds
- B) Measures elapsed time
- C) Speeds up the program
- D) Returns the current time

**Question 28:** Approximately how many seconds does this program take to run?
- A) 0 seconds
- B) 2 seconds
- C) It varies randomly
- D) 10 seconds


