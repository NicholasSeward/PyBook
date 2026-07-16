# Default Arguments

## Overview
Default arguments let you make some parameters optional in your functions. They provide sensible values when the caller doesn't specify them.

## What are Default Arguments?

You can give parameters default values using `parameter=default_value`. This makes the parameter optional.

```python
# Function with default arguments
def greet(name, greeting="Hello"):
    return f"{greeting}, {name}!"

# Using default greeting
print(greet("Alice"))           # Output: Hello, Alice!

# Overriding the default
print(greet("Bob", "Good morning"))  # Output: Good morning, Bob!
```

## Basic Examples

### Simple Default Values
```python
def create_user(username, is_active=True, role="user"):
    """Create a user with optional settings."""
    user = {"username": username}
    
    if is_active:
        user["status"] = "active"
    else:
        user["status"] = "inactive"
    
    user["role"] = role
    return user

# Test different combinations
print(create_user("alice123"))                    # Uses all defaults
print(create_user("bob456", False))               # Override is_active
print(create_user("charlie789", True, "admin"))   # Override both defaults
```

### Multiple Default Arguments
```python
def calculate_grade(scores, passing_threshold=60, curve=0):
    """Calculate grade with optional parameters."""
    if not scores:
        return 0
    
    average = sum(scores) / len(scores)
    final_grade = average + curve
    
    if final_grade >= passing_threshold:
        status = "Pass"
    else:
        status = "Fail"
    
    return {"grade": final_grade, "status": status}

# Test with different options
test_scores = [75, 80, 85, 90]
print(calculate_grade(test_scores))                    # Default threshold and no curve
print(calculate_grade(test_scores, 70))                # Custom threshold
print(calculate_grade(test_scores, 70, 5))            # Custom threshold and curve
```

## Common Use Cases

### 1. Configuration Settings
```python
def connect_database(
    host="localhost",
    port=5432,
    username="admin",
    timeout=30
):
    """Connect to database with default settings."""
    print(f"Connecting to {host}:{port} as {username}")
    print(f"Timeout: {timeout} seconds")
    return f"Connected to {host}:{port}"

# Use all defaults
print(connect_database())

# Override some defaults
print(connect_database(host="192.168.1.100", username="developer"))
```

### 2. Formatting Options
```python
def format_number(
    number,
    decimal_places=2,
    add_commas=True,
    currency_symbol=""
):
    """Format a number with various options."""
    formatted = f"{number:.{decimal_places}f}"
    
    if add_commas:
        # Simple comma insertion for demonstration
        parts = formatted.split('.')
        if len(parts[0]) > 3:
            parts[0] = f"{int(parts[0]):,}"
        formatted = '.'.join(parts)
    
    if currency_symbol:
        formatted = f"{currency_symbol}{formatted}"
    
    return formatted

# Test different formatting options
number = 1234567.89
print(f"Basic: {format_number(number)}")
print(f"No commas: {format_number(number, add_commas=False)}")
print(f"Currency: {format_number(number, currency_symbol='$')}")
```

## Important Rules

### Rule 1: Default Arguments Must Come Last
```python
# This is valid - required parameters first, then optional ones
def valid_function(required1, required2, optional1="default", optional2="default"):
    return f"{required1}, {required2}, {optional1}, {optional2}"

# This works
print(valid_function("a", "b"))
print(valid_function("a", "b", "custom1"))

# This would cause a syntax error:
# def invalid_function(required1, optional1="default", required2):
#     pass
```

### Rule 2: Use None for Mutable Defaults
```python
# Problem: Default list is shared between all calls
def add_to_list_bad(item, my_list=[]):
    my_list.append(item)
    return my_list

# This can cause unexpected behavior!
print(add_to_list_bad(1))  # [1]
print(add_to_list_bad(2))  # [1, 2] - remembers previous items!

# Solution: Use None as default
def add_to_list_good(item, my_list=None):
    if my_list is None:
        my_list = []  # Create a new list each time
    my_list.append(item)
    return my_list

# Now it works correctly
print(add_to_list_good(1))  # [1]
print(add_to_list_good(2))  # [2]
```

## Best Practices

### 1. Choose Sensible Defaults
```python
# Good - sensible defaults
def send_email(
    to_address,
    subject,
    body,
    from_address="noreply@company.com",  # Clear default
    priority="normal",                    # Clear default
    cc=None,                              # None for optional
    bcc=None                              # None for optional
):
    print(f"Sending email to: {to_address}")
    print(f"Subject: {subject}")
    print(f"From: {from_address}")
    print(f"Priority: {priority}")
    
    if cc:
        print(f"CC: {cc}")
    if bcc:
        print(f"BCC: {bcc}")
    
    return "Email sent successfully"

# Test with different combinations
send_email("user@example.com", "Hello", "This is a test")
send_email("manager@example.com", "Urgent", "Please review", priority="high")
```

### 2. Use Descriptive Default Values
```python
# Good - descriptive defaults
def process_data(
    data,
    filter_func=None,      # None means no filtering
    sort_key=None,         # None means no sorting
    limit=None             # None means no limit
):
    """Process data with optional operations."""
    result = data.copy()
    
    if filter_func:
        result = [item for item in result if filter_func(item)]
    
    if sort_key:
        result.sort(key=sort_key)
    
    if limit:
        result = result[:limit]
    
    return result

# Test with different options
numbers = [5, 2, 8, 1, 9, 3, 7, 4, 6]
print(f"Original: {numbers}")
print(f"Filtered (even only): {process_data(numbers, filter_func=lambda x: x % 2 == 0)}")
print(f"Sorted: {process_data(numbers, sort_key=lambda x: x)}")
print(f"Limited: {process_data(numbers, limit=5)}")
```

## Summary

Default arguments help you:

✅ **Make functions more flexible** - callers can use defaults or override them  
✅ **Reduce code duplication** - one function handles many use cases  
✅ **Improve readability** - function calls show only what's different from defaults  
✅ **Provide sensible defaults** - functions work out of the box  

**Key rules to remember:**
1. Default arguments come after required arguments
2. Use `None` as default for mutable objects (lists, dictionaries)
3. Choose sensible, descriptive default values
4. Keep the number of default arguments reasonable
5. Document what each default represents

**Think of it this way:**
- **Required parameters** = ingredients you must provide
- **Default parameters** = ingredients that are already in the kitchen
- **Function call** = you only need to bring the missing ingredients

Default arguments make your functions more user-friendly and reduce the chance of errors!
