# Formatting Strings (f-strings)

## Overview
F-strings (formatted string literals) are a modern, readable way to format strings in Python. They were introduced in Python 3.6 and are now the recommended method for string formatting.

## What are F-strings?

F-strings are strings prefixed with the letter `f` that allow you to embed Python expressions inside string literals using curly braces `{}`.

## Basic Syntax

```python
name = "Alice"
age = 25

# F-string format
message = f"My name is {name} and I am {age} years old"
print(message)
# Output: My name is Alice and I am 25 years old
```

## Why Use F-strings?

- **Readable**: Easy to understand what the output will be
- **Efficient**: Faster than other string formatting methods
- **Powerful**: Can include any valid Python expression
- **Modern**: Python 3.6+ standard

## Basic Usage Examples

### Simple Variable Insertion
```python
first_name = "John"
last_name = "Doe"
full_name = f"{first_name} {last_name}"
print(full_name)  # Output: John Doe
```

### Expressions Inside F-strings
```python
x = 10
y = 5
result = f"The sum of {x} and {y} is {x + y}"
print(result)  # Output: The sum of 10 and 5 is 15
```

### Method Calls
```python
text = "hello world"
formatted = f"Original: {text}, Uppercase: {text.upper()}"
print(formatted)  # Output: Original: hello world, Uppercase: HELLO WORLD
```

## Advanced Features

### Formatting Numbers
```python
pi = 3.14159
radius = 5
area = pi * radius ** 2

# Format to 2 decimal places
formatted_area = f"The area is {area:.2f}"
print(formatted_area)  # Output: The area is 78.54

# Format with commas for thousands
population = 1234567
formatted_pop = f"Population: {population:,}"
print(formatted_pop)  # Output: Population: 1,234,567
```

### Alignment and Width
```python
name = "Bob"
score = 95

# Left align with width of 10
left_aligned = f"Name: {name:<10} Score: {score}"
print(left_aligned)  # Output: Name: Bob        Score: 95

# Right align with width of 10
right_aligned = f"Name: {name:>10} Score: {score}"
print(right_aligned)  # Output: Name:        Bob Score: 95

# Center align with width of 10
center_aligned = f"Name: {name:^10} Score: {score}"
print(center_aligned)  # Output: Name:    Bob     Score: 95
```

### Using Different Data Types
```python
# Lists
fruits = ["apple", "banana", "orange"]
fruit_list = f"Fruits: {fruits}"
print(fruit_list)  # Output: Fruits: ['apple', 'banana', 'orange']

# Dictionaries
person = {"name": "Alice", "age": 30}
person_info = f"Person: {person['name']}, Age: {person['age']}"
print(person_info)  # Output: Person: Alice, Age: 30

# Boolean values
is_student = True
status = f"Student status: {is_student}"
print(status)  # Output: Student status: True
```

## Common Use Cases

### User Interface Messages
```python
username = "john_doe"
login_time = "14:30"
welcome_msg = f"Welcome back, {username}! Last login: {login_time}"
print(welcome_msg)
```

### Error Messages
```python
expected = "string"
received = "integer"
error_msg = f"TypeError: Expected {expected}, but received {received}"
print(error_msg)
```

### Data Reports
```python
total_sales = 1250.75
num_orders = 15
avg_order = total_sales / num_orders

report = f"""
Sales Report:
Total Sales: ${total_sales:,.2f}
Number of Orders: {num_orders}
Average Order Value: ${avg_order:.2f}
"""
print(report)
```

## Comparison with Other Methods

### Old-style % formatting
```python
# Old way (not recommended)
name = "Alice"
age = 25
message = "My name is %s and I am %d years old" % (name, age)
```

### .format() method
```python
# .format() method
message = "My name is {} and I am {} years old".format(name, age)
```

### F-strings (recommended)
```python
# F-strings (recommended)
message = f"My name is {name} and I am {age} years old"
```

## Best Practices

1. **Use f-strings for simple formatting**: They're the most readable option
2. **Keep expressions simple**: Avoid complex logic inside f-strings
3. **Use descriptive variable names**: Makes f-strings more readable
4. **Format numbers appropriately**: Use `.2f` for currency, `:,` for large numbers
5. **Consider readability**: Don't make f-strings too long or complex

## Limitations

- **Python 3.6+ only**: Won't work in older Python versions
- **Expression complexity**: Keep expressions simple for readability
- **Debugging**: Can be harder to debug very complex f-strings

## Summary

F-strings provide a clean, readable way to format strings in Python. They're faster than other methods and make code more maintainable. Use them whenever you need to combine variables and text in a readable way.
