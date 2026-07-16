# Function Signatures and Annotations

## Overview
Function signatures and annotations help make your code more readable and self-documenting. They show what a function expects and what it returns.

## What is a Function Signature?

A function signature is the "blueprint" of a function - it shows:
- The function name
- What parameters it takes
- What it returns

Think of it like a recipe card that lists ingredients and expected results.

```python
# Basic function signature
def greet(name, age):
    return f"Hello {name}, you are {age} years old"

# Function name: greet
# Parameters: name, age
# Return: string
```

## Function Annotations

Annotations add extra information about types and purpose. They make code clearer and help catch errors early.

```python
# Function with type annotations
def calculate_area(length: float, width: float) -> float:
    """Calculate the area of a rectangle."""
    return length * width

# length: float means the parameter should be a float
# -> float means the function returns a float
```

## Different Types of Annotations

### String Annotations
```python
def process_user(name: "user's full name", age: "user's age in years") -> "greeting message":
    return f"Hello {name}, you are {age} years old"
```

### List and Dictionary Annotations
```python
def get_even_numbers(numbers: list) -> list:
    return [num for num in numbers if num % 2 == 0]

def create_user_profile(name: str, age: int) -> dict:
    return {"name": name, "age": age, "status": "active"}
```

## Why Use Annotations?

1. **Self-documenting code** - Others can see what your function expects
2. **Better IDE support** - Your editor can catch type mismatches
3. **Easier debugging** - You know what types to expect
4. **Documentation generation** - Tools can create docs automatically

## Common Patterns

### Basic Types
```python
def add_numbers(a: int, b: int) -> int:
    return a + b

def get_name() -> str:
    return "Alice"

def is_valid(age: int) -> bool:
    return age >= 0
```

### Optional Parameters
```python
def greet_user(name: str, title: str = None) -> str:
    if title:
        return f"Hello {title} {name}!"
    else:
        return f"Hello {name}!"
```

## Best Practices

### 1. Use Descriptive Parameter Names
```python
def calculate_distance(
    x1: float, y1: float,  # Point 1 coordinates
    x2: float, y2: float   # Point 2 coordinates
) -> float:
    return ((x2 - x1) ** 2 + (y2 - y1) ** 2) ** 0.5
```

### 2. Keep Annotations Simple
```python
# Good - simple and clear
def process_data(data: list) -> list:
    return [item * 2 for item in data]

# Less good - too complex for beginners
def process_data(data: List[Union[int, float]]) -> List[Union[int, float]]:
    return [item * 2 for item in data]
```

## Examples in Practice

### Student Grade Calculator
```python
def calculate_grade(scores: list, weights: list = None) -> float:
    """Calculate weighted grade from a list of scores."""
    if weights is None:
        # Equal weights
        return sum(scores) / len(scores)
    
    # Calculate weighted sum
    weighted_sum = sum(score * weight for score, weight in zip(scores, weights))
    return weighted_sum
```

### Text Processing
```python
def analyze_text(text: str) -> dict:
    """Analyze text and return statistics."""
    words = text.split()
    return {
        "characters": len(text),
        "words": len(words),
        "average_word_length": len(text) / len(words) if words else 0
    }
```

## Summary

Function signatures and annotations help you:

✅ **Write clearer code** - others can see what your function expects  
✅ **Catch errors early** - IDEs can warn about type mismatches  
✅ **Document your code** - annotations serve as inline documentation  
✅ **Improve IDE support** - better autocomplete and error detection  

**Key points to remember:**
1. Use `parameter: type` for parameter annotations
2. Use `-> type` for return annotations
3. Annotations are optional but highly recommended
4. Keep annotations simple and readable
5. Use descriptive parameter names

**Think of it this way:**
- **Function signature** = recipe ingredients list
- **Annotations** = ingredient types and measurements
- **Return annotation** = what the final dish should look like

Start using annotations early - they become more valuable as your programs grow!
