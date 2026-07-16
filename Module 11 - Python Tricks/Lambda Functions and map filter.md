# Lambda Functions and map/filter

## What are Lambda Functions?

Lambda functions are small, anonymous functions that you can define in one line. They're perfect for simple operations that you only need once.

## Basic Lambda Syntax

```python
# Regular function
def add_five(x):
    return x + 5

# Lambda function (same thing)
add_five = lambda x: x + 5

# Use them the same way
print(add_five(3))  # 8
```

## Lambda with Multiple Arguments

```python
# Add two numbers
add = lambda x, y: x + y
print(add(5, 3))  # 8

# Find maximum
max_num = lambda x, y: x if x > y else y
print(max_num(10, 7))  # 10
```

## Lambda with map()

The `map()` function applies a function to every item in a list.

```python
# Double every number in a list
numbers = [1, 2, 3, 4, 5]
doubled = list(map(lambda x: x * 2, numbers))
print(doubled)  # [2, 4, 6, 8, 10]

# Convert strings to uppercase
words = ["hello", "world", "python"]
uppercase = list(map(lambda word: word.upper(), words))
print(uppercase)  # ['HELLO', 'WORLD', 'PYTHON']
```

## Lambda with filter()

The `filter()` function keeps only items that make a condition true.

```python
# Keep only even numbers
numbers = [1, 2, 3, 4, 5, 6, 7, 8]
evens = list(filter(lambda x: x % 2 == 0, numbers))
print(evens)  # [2, 4, 6, 8]

# Keep only words longer than 3 characters
words = ["cat", "dog", "elephant", "bird", "ant"]
long_words = list(filter(lambda word: len(word) > 3, words))
print(long_words)  # ['elephant', 'bird']
```

## Combining map() and filter()

```python
# Double only the even numbers
numbers = [1, 2, 3, 4, 5, 6]
result = list(map(lambda x: x * 2, filter(lambda x: x % 2 == 0, numbers)))
print(result)  # [4, 8, 12]
```

## When to Use Lambda

**Use lambda for:**
- Simple one-line operations
- Functions you only need once
- map() and filter() operations

**Use regular functions for:**
- Complex logic
- Functions you'll reuse
- Better readability

## Key Points

- **Lambda syntax**: `lambda arguments: expression`
- **map()**: Apply function to every item
- **filter()**: Keep items that meet condition
- **Anonymous**: No function name needed
- **One line**: Keep expressions simple
