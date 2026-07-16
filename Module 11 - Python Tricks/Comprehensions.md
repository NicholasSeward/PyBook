# Comprehensions

## What are Comprehensions?

Comprehensions are a concise way to create lists, dictionaries, and sets. They're like shortcuts for common operations.

## List Comprehensions

### Basic Syntax
```python
# Old way with a loop
squares = []
for i in range(5):
    squares.append(i ** 2)
print(squares)  # [0, 1, 4, 9, 16]

# New way with comprehension
squares = [i ** 2 for i in range(5)]
print(squares)  # [0, 1, 4, 9, 16]
```

### With Conditions
```python
# Only even numbers
evens = [i for i in range(10) if i % 2 == 0]
print(evens)  # [0, 2, 4, 6, 8]

# Only positive numbers
numbers = [-2, -1, 0, 1, 2]
positives = [n for n in numbers if n > 0]
print(positives)  # [1, 2]
```

### Advanced: Multiple Conditions
```python
# Numbers that are even AND greater than 5
filtered = [i for i in range(20) if i % 2 == 0 and i > 5]
print(filtered)  # [6, 8, 10, 12, 14, 16, 18]

# Strings that start with 'a' OR are longer than 3 characters
words = ["apple", "banana", "cat", "dog", "ant"]
filtered = [w for w in words if w.startswith('a') or len(w) > 3]
print(filtered)  # ['apple', 'banana', 'ant']
```

## Dictionary Comprehensions

```python
# Create dictionary from list
numbers = [1, 2, 3, 4, 5]
squares_dict = {n: n**2 for n in numbers}
print(squares_dict)  # {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}

# With condition
even_squares = {n: n**2 for n in numbers if n % 2 == 0}
print(even_squares)  # {2: 4, 4: 16}
```

## Set Comprehensions

```python
# Create set of unique characters
word = "hello"
unique_chars = {char for char in word}
print(unique_chars)  # {'h', 'e', 'l', 'o'}

# With condition
vowels = {char for char in word if char in 'aeiou'}
print(vowels)  # {'e', 'o'}
```

## Key Points

- **List comprehension**: `[expression for item in iterable if condition]`
- **Dictionary comprehension**: `{key: value for item in iterable if condition}`
- **Set comprehension**: `{expression for item in iterable if condition}`
- **Conditions are optional**: Use `if` to filter items
- **Multiple conditions**: Use `and`/`or` for complex filtering
