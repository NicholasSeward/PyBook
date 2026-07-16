# Iterators and Generators

## What are Iterators?

Iterators are objects that let you go through a collection one item at a time. Lists, strings, and other collections are iterable.

## Basic Iteration

```python
# Lists are iterable
numbers = [1, 2, 3, 4, 5]
for num in numbers:
    print(num)

# Strings are iterable
word = "hello"
for char in word:
    print(char)
```

## Creating Iterators

```python
# Get iterator from list
numbers = [1, 2, 3, 4, 5]
iterator = iter(numbers)

# Get next item
print(next(iterator))  # 1
print(next(iterator))  # 2
print(next(iterator))  # 3

# When you run out of items
try:
    print(next(iterator))  # 4
    print(next(iterator))  # 5
    print(next(iterator))  # Error!
except StopIteration:
    print("No more items")
```

## What are Generators?

Generators are functions that create iterators. They use `yield` instead of `return` and remember where they left off.

## Basic Generator

```python
def number_generator():
    yield 1
    yield 2
    yield 3
    yield 4
    yield 5

# Use the generator
gen = number_generator()
print(next(gen))  # 1
print(next(gen))  # 2
print(next(gen))  # 3
```

## Generator with Loop

```python
def count_up_to(n):
    for i in range(1, n + 1):
        yield i

# Use it
counter = count_up_to(5)
for num in counter:
    print(num)  # Prints 1, 2, 3, 4, 5
```

## Generator Expression

```python
# Create generator expression (like list comprehension but with parentheses)
squares = (x**2 for x in range(5))

# Use it
for square in squares:
    print(square)  # Prints 0, 1, 4, 9, 16
```

## Why Use Generators?

**Memory efficient**: Generators don't store all values in memory at once.

```python
# List comprehension (stores all in memory)
big_list = [x**2 for x in range(1000000)]

# Generator expression (only stores one at a time)
big_gen = (x**2 for x in range(1000000))

# Both do the same thing, but generator uses less memory
```

## Key Points

- **Iterators**: Go through collections one item at a time
- **Generators**: Functions that create iterators
- **yield**: Pauses function and returns value
- **Memory efficient**: Don't store all values at once
- **next()**: Get next item from iterator
- **StopIteration**: Error when no more items
