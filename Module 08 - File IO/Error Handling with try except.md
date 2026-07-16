# Error Handling with try-except

## What is Error Handling?

Error handling prevents your program from crashing when something goes wrong. The `try-except` block catches errors and handles them gracefully.

## Basic Structure

### Generic Error Handling
```python
try:
    # Code that might cause an error
    number = int("abc")
    print(f"Number: {number}")
except:
    # Code that runs if any error occurs
    print("Something went wrong!")
    print("Program continues...")
```

### Specific Error Handling
```python
try:
    number = int("abc")
    print(f"Number: {number}")
except ValueError:
    print("That's not a valid number!")
except TypeError:
    print("Wrong type!")
except Exception as e:
    print(f"Unexpected error: {e}")
```

## Common Error Types

### ValueError
```python
try:
    age = int("twenty")
    print(f"Age: {age}")
except ValueError:
    print("Please enter a valid number for age")
```

### FileNotFoundError
```python
try:
    with open('nonexistent.txt', 'r') as file:
        content = file.read()
except FileNotFoundError:
    print("File not found. Creating a new one.")
    with open('nonexistent.txt', 'w') as file:
        file.write("This is a new file")
```

### ZeroDivisionError
```python
try:
    result = 10 / 0
    print(f"Result: {result}")
except ZeroDivisionError:
    print("Cannot divide by zero!")
    result = 0
```

## Real Examples

### User Input Validation
```python
def get_user_age():
    while True:
        try:
            age = int(input("Enter your age: "))
            return age
        except ValueError:
            print("Please enter a valid number")

# Test the function
user_age = get_user_age()
print(f"User age: {user_age}")
```

### Safe File Reading
```python
def read_file_safely(filename):
    try:
        with open(filename, 'r') as file:
            return file.read()
    except FileNotFoundError:
        print(f"File '{filename}' not found")
        return None

# Test the function
content = read_file_safely('test.txt')
if content:
    print("File content:", content)
else:
    print("Could not read file")
```

## Advanced Features (for Advanced Users)

### else Clause
```python
try:
    number = int(input("Enter a number: "))
except ValueError:
    print("Invalid input")
else:
    # This runs only if no error occurred
    print(f"You entered: {number}")
```

### finally Clause
```python
try:
    file = open('data.txt', 'r')
    content = file.read()
except FileNotFoundError:
    print("File not found")
finally:
    # This always runs, even if there's an error
    if 'file' in locals():
        file.close()
    print("File handling completed")
```

## Key Points

- **`try-except`** - catches and handles errors gracefully
- **Generic except** - catches any error (use sparingly)
- **Specific except** - handle different error types appropriately
- **`else` and `finally`** - advanced features for experienced users
- **Always handle errors** - don't let your program crash

## Summary

✅ **Error handling** - prevents program crashes  
✅ **try-except** - catch and handle errors gracefully  
✅ **Generic except** - catch any error  
✅ **Specific except** - handle different error types  
✅ **Advanced features** - else/finally for experienced users  

Error handling makes your programs more robust!
