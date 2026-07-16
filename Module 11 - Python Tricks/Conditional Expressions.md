# Conditional Expressions

## What are Conditional Expressions?

Conditional expressions (also called ternary operators) let you write simple if-else statements in one line. They're perfect for simple decisions.

## Basic Syntax

```python
# Old way with if-else
if age >= 18:
    status = "adult"
else:
    status = "minor"

# New way with conditional expression
status = "adult" if age >= 18 else "minor"
```

## More Examples

### Simple Comparisons
```python
# Check if number is positive or negative
number = 5
result = "positive" if number > 0 else "negative or zero"
print(result)  # "positive"

# Check if string is empty
text = "hello"
length_status = "has content" if text else "empty"
print(length_status)  # "has content"
```

### With Functions
```python
# Return different values based on condition
def get_message(score):
    return "Pass" if score >= 70 else "Fail"

print(get_message(85))  # "Pass"
print(get_message(65))  # "Fail"
```

### Nested Conditional Expressions
```python
# Multiple conditions
grade = 85
letter_grade = "A" if grade >= 90 else "B" if grade >= 80 else "C" if grade >= 70 else "F"
print(letter_grade)  # "B"
```

## When to Use

**Use conditional expressions for:**
- Simple yes/no decisions
- One-line assignments
- Simple function returns

**Use regular if-else for:**
- Complex logic
- Multiple statements
- Better readability

## Key Points

- **Syntax**: `value_if_true if condition else value_if_false`
- **One line**: Perfect for simple decisions
- **Readable**: Keep it simple and clear
- **Alternative**: Use regular if-else for complex logic
