# Casting between Types

## Overview
Type casting (or type conversion) is the process of converting a value from one data type to another. Python provides built-in functions to perform these conversions safely.

## Why Cast Types?

- **Data Processing**: Convert user input to the right type
- **Mathematical Operations**: Ensure compatible types for calculations
- **API Requirements**: Match expected data types
- **Data Validation**: Check if conversion is possible

## Built-in Type Conversion Functions

### Numeric Conversions

#### int() - Convert to Integer
```python
# String to integer
age = "25"
age_int = int(age)
print(age_int)  # Output: 25
print(type(age_int))  # Output: <class 'int'>

# Float to integer (truncates decimal part)
price = 19.99
price_int = int(price)
print(price_int)  # Output: 19

# Boolean to integer
true_val = True
false_val = False
print(int(true_val))   # Output: 1
print(int(false_val))  # Output: 0
```

#### float() - Convert to Float
```python
# String to float
height = "5.8"
height_float = float(height)
print(height_float)  # Output: 5.8

# Integer to float
count = 42
count_float = float(count)
print(count_float)  # Output: 42.0

# Boolean to float
print(float(True))   # Output: 1.0
print(float(False))  # Output: 0.0
```

### String Conversions

#### str() - Convert to String
```python
# Number to string
number = 42
number_str = str(number)
print(number_str)  # Output: "42"
print(type(number_str))  # Output: <class 'str'>

# Float to string
pi = 3.14159
pi_str = str(pi)
print(pi_str)  # Output: "3.14159"

# Boolean to string
is_valid = True
is_valid_str = str(is_valid)
print(is_valid_str)  # Output: "True"

# List to string
fruits = ["apple", "banana"]
fruits_str = str(fruits)
print(fruits_str)  # Output: "['apple', 'banana']"
```

### Boolean Conversions

#### bool() - Convert to Boolean
```python
# Number to boolean (0 is False, non-zero is True)
print(bool(0))      # Output: False
print(bool(1))      # Output: True
print(bool(-5))     # Output: True
print(bool(3.14))   # Output: True

# String to boolean (empty string is False, non-empty is True)
print(bool(""))     # Output: False
print(bool("hello")) # Output: True
print(bool("0"))    # Output: True (non-empty string)

# List to boolean (empty list is False, non-empty is True)
print(bool([]))     # Output: False
print(bool([1, 2])) # Output: True

# None to boolean
print(bool(None))   # Output: False
```

## Common Casting Scenarios

### User Input Processing
```python
# Get user input (always returns string)
user_age = input("Enter your age: ")  # User types "25"
age = int(user_age)  # Convert to integer

if age >= 18:
    print("You are an adult")
else:
    print("You are a minor")
```

### Mathematical Operations
```python
# Ensure both operands are the same type
x = 5
y = "3"

# Convert string to integer for addition
result = x + int(y)
print(result)  # Output: 8

# Or convert both to float for division
result = float(x) / float(y)
print(result)  # Output: 1.6666666666666667
```

### Data Validation
```python
def validate_age(age_input):
    try:
        age = int(age_input)
        if 0 <= age <= 120:
            return True, age
        else:
            return False, "Age must be between 0 and 120"
    except ValueError:
        return False, "Invalid age format"

# Test the function
is_valid, result = validate_age("25")
print(f"Valid: {is_valid}, Result: {result}")  # Output: Valid: True, Result: 25

is_valid, result = validate_age("abc")
print(f"Valid: {is_valid}, Result: {result}")  # Output: Valid: False, Result: Invalid age format
```

## Handling Conversion Errors

### Using try-except
```python
def safe_convert(value, target_type):
    try:
        return target_type(value)
    except (ValueError, TypeError):
        return None

# Safe conversions
result1 = safe_convert("123", int)      # Returns: 123
result2 = safe_convert("abc", int)      # Returns: None
result3 = safe_convert("3.14", float)   # Returns: 3.14
result4 = safe_convert("", bool)        # Returns: False
```

### Checking Convertibility
```python
def can_convert(value, target_type):
    try:
        target_type(value)
        return True
    except (ValueError, TypeError):
        return False

# Check if conversion is possible
print(can_convert("123", int))      # Output: True
print(can_convert("abc", int))      # Output: False
print(can_convert("3.14", float))   # Output: True
print(can_convert("", int))         # Output: False
```

## Advanced Casting

### List and Tuple Conversions
```python
# String to list of characters
text = "hello"
char_list = list(text)
print(char_list)  # Output: ['h', 'e', 'l', 'l', 'o']

# String to tuple
char_tuple = tuple(text)
print(char_tuple)  # Output: ('h', 'e', 'l', 'l', 'o')

# List to tuple
numbers = [1, 2, 3, 4, 5]
numbers_tuple = tuple(numbers)
print(numbers_tuple)  # Output: (1, 2, 3, 4, 5)
```

### Dictionary Conversions
```python
# List of tuples to dictionary
pairs = [("name", "Alice"), ("age", 30)]
person_dict = dict(pairs)
print(person_dict)  # Output: {'name': 'Alice', 'age': 30}

# List of lists to dictionary
pairs_list = [["a", 1], ["b", 2]]
dict_from_list = dict(pairs_list)
print(dict_from_list)  # Output: {'a': 1, 'b': 2}
```

## Best Practices

1. **Always validate input**: Check if conversion is possible before attempting it
2. **Use appropriate types**: Choose the right type for your data
3. **Handle errors gracefully**: Use try-except blocks for user input
4. **Be explicit**: Make your intentions clear with explicit conversions
5. **Consider performance**: Avoid unnecessary conversions in loops

## Common Pitfalls

### Loss of Precision
```python
# Float to int truncates decimal part
pi = 3.14159
pi_int = int(pi)  # Loses precision
print(pi_int)  # Output: 3
```

### String to Number Errors
```python
# This will raise ValueError
try:
    invalid_number = int("12.34")
except ValueError as e:
    print(f"Error: {e}")  # Output: Error: invalid literal for int() with base 10: '12.34'
```

### Boolean Conversion Surprises
```python
# These might be surprising
print(bool("0"))     # Output: True (non-empty string)
print(bool(0))       # Output: False (zero)
print(bool("False")) # Output: True (non-empty string)
```

## Summary

Type casting is essential for working with different data types in Python. Use the built-in conversion functions (`int()`, `float()`, `str()`, `bool()`) and always handle potential errors with try-except blocks. Remember that some conversions may lose data (like float to int) and always validate user input before conversion.
