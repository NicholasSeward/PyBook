# While Loops

## Overview

A `while` loop repeats code **as long as a condition is true**. Use `while` when you **don’t know in advance** how many times you need to repeat something.

Think of it like: “Keep going **while** this is still true.”

---

## Basic Pattern

```python
while condition:
    # loop body (repeats)
    ...
```

Key idea:
- If the condition starts as `False`, the loop body runs **zero times**.
- If the condition never becomes `False`, you get an **infinite loop**.

---

## Example 1: Countdown

```python
n = 5
while n > 0:
    print(n)
    n = n - 1
print("Blastoff!")
```

**Output:**
```
5
4
3
2
1
Blastoff!
```

Why it stops:
- `n` changes each time.
- Eventually `n > 0` becomes false.

---

## Example 2: Keep Asking Until Valid Input

This is a common use of `while`: keep asking until the user gives a valid answer.

```python
choice = ""
while choice != "y" and choice != "n":
    choice = input("Continue? (y/n): ").strip().lower()

print(f"You chose: {choice}")
```

Notes:
- The condition uses **boolean logic**: `and`
- `.strip().lower()` helps handle input like `" Y "` or `"N"`

---

## Example 3: Sentinel Loop (Stop When the User Types a Special Word)

```python
text = ""
while text != "quit":
    text = input("Type something (or 'quit' to stop): ").strip().lower()
    if text != "quit":
        print(f"You typed: {text}")

print("Goodbye!")
```

This pattern is called a **sentinel loop**:
- the sentinel value here is `"quit"`

---

## Example 4: Accumulator with a While Loop

```python
total = 0
count = 0

number = int(input("Enter a number (enter 0 to stop): "))
while number != 0:
    total += number
    count += 1
    number = int(input("Enter a number (enter 0 to stop): "))

print(f"Count: {count}")
print(f"Total: {total}")
```

---

## Common Mistakes

### 1. Forgetting to update the variable

```python
# BUG: n never changes, so this loop never ends
n = 5
while n > 0:
    print(n)
```

### 2. Wrong condition (off-by-one)

```python
# This prints 5,4,3,2,1,0 (maybe not what you want)
n = 5
while n >= 0:
    print(n)
    n -= 1
```

### 3. Not converting input types

```python
# input() returns a string, so "10" > "2" is not numeric comparison
text = input("Enter a number: ")
```

If you need a number, cast it:

```python
number = int(input("Enter a number: "))
```

---

## Summary

✅ Use `while` when the number of repetitions is **unknown** ahead of time  
✅ Make sure something changes so the loop can eventually stop  
✅ `while` is great for **input validation** and **sentinel loops**  

