# Loop Control: break, continue, pass

## Overview
Sometimes you need to control how loops behave. Python gives you three tools: `break`, `continue`, and `pass`.

## break - Stop the Loop

`break` immediately stops the loop and continues with the next code after the loop.

```python
# Find the first number greater than 5
numbers = [1, 3, 7, 2, 9, 4]
for num in numbers:
    if num > 5:
        print(f"Found: {num}")
        break  # Stop looking, we found one!
    print(f"Checking {num}...")

print("Loop finished")
```

**Output:**
```
Checking 1...
Checking 3...
Found: 7
Loop finished
```

## continue - Skip to Next Iteration

`continue` skips the rest of the current iteration and goes to the next one.

```python
# Print only even numbers
numbers = [1, 2, 3, 4, 5, 6]
for num in numbers:
    if num % 2 != 0:  # If odd
        continue        # Skip to next number
    print(f"Even number: {num}")

print("Done")
```

**Output:**
```
Even number: 2
Even number: 4
Even number: 6
Done
```

## pass - Do Nothing

`pass` does nothing. It's useful when you need a placeholder.

```python
# Check if numbers are positive, negative, or zero
numbers = [5, -3, 0, 8, -1]
for num in numbers:
    if num > 0:
        print(f"{num} is positive")
    elif num < 0:
        print(f"{num} is negative")
    else:
        pass  # Do nothing for zero

print("Finished checking")
```

**Output:**
```
5 is positive
-3 is negative
8 is positive
-1 is negative
Finished checking
```

## Real Example: User Input

```python
# Keep asking for a number until user enters 'quit'
while True:
    user_input = input("Enter a number (or 'quit' to stop): ")
    
    if user_input.lower() == 'quit':
        break  # Exit the loop
    
    if user_input == '':
        continue  # Skip empty input
    
    try:
        number = int(user_input)
        print(f"You entered: {number}")
    except ValueError:
        print("That's not a valid number!")
        continue  # Try again

print("Goodbye!")
```

## When to Use Each

- **`break`** - When you want to stop the loop early
- **`continue`** - When you want to skip the current item
- **`pass`** - When you need a placeholder (rare in simple programs)

## Summary

✅ **`break`** - stops the loop completely  
✅ **`continue`** - skips to the next iteration  
✅ **`pass`** - does nothing (placeholder)  

These tools give you more control over how your loops work!
