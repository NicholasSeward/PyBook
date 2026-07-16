# zip and Unpacking

## What is zip()?

The `zip()` function combines multiple lists into pairs. It's like zipping up a jacket - you bring two sides together.

## Basic zip()

```python
# Combine two lists
names = ["Alice", "Bob", "Charlie"]
ages = [25, 30, 35]

# Zip them together
pairs = list(zip(names, ages))
print(pairs)  # [('Alice', 25), ('Bob', 30), ('Charlie', 35)]

# Loop through pairs
for name, age in zip(names, ages):
    print(f"{name} is {age} years old")
```

## Unpacking

Unpacking lets you assign multiple values at once.

```python
# Unpack a tuple
person = ("Alice", 25, "Engineer")
name, age, job = person
print(f"Name: {name}, Age: {age}, Job: {job}")

# Unpack from zip
for name, age in zip(names, ages):
    print(f"{name}: {age}")
```

## Different Length Lists

When lists have different lengths, `zip()` stops at the shortest one.

```python
# Different lengths
names = ["Alice", "Bob", "Charlie", "David"]
ages = [25, 30]  # Shorter list

# Only pairs up to shortest length
pairs = list(zip(names, ages))
print(pairs)  # [('Alice', 25), ('Bob', 30)]
```

## Multiple Lists

You can zip more than two lists together.

```python
# Three lists
names = ["Alice", "Bob", "Charlie"]
ages = [25, 30, 35]
cities = ["NYC", "LA", "Chicago"]

# Zip all three
triples = list(zip(names, ages, cities))
print(triples)  # [('Alice', 25, 'NYC'), ('Bob', 30, 'LA'), ('Charlie', 35, 'Chicago')]

# Loop through all three
for name, age, city in zip(names, ages, cities):
    print(f"{name} is {age} and lives in {city}")
```

## Unzipping

You can also "unzip" - separate the pairs back into separate lists.

```python
# Zip first
pairs = list(zip(names, ages))

# Unzip back to separate lists
unzipped_names, unzipped_ages = zip(*pairs)
print(list(unzipped_names))  # ['Alice', 'Bob', 'Charlie']
print(list(unzipped_ages))   # [25, 30, 35]
```

## The * Operator (Unpacking)

The `*` operator has several uses in Python unpacking.

### Unpacking Lists/Tuples
```python
# Unpack a list
numbers = [1, 2, 3, 4, 5]
first, *middle, last = numbers
print(first)   # 1
print(middle)  # [2, 3, 4]
print(last)    # 5

# Unpack with * in different positions
first, second, *rest = [1, 2, 3, 4, 5]
print(rest)  # [3, 4, 5]

*start, end = [1, 2, 3, 4, 5]
print(start)  # [1, 2, 3, 4]
print(end)    # 5
```

### Function Arguments
```python
# Unpack list as separate arguments
def add_three(a, b, c):
    return a + b + c

numbers = [10, 20, 30]
result = add_three(*numbers)  # Same as add_three(10, 20, 30)
print(result)  # 60

# Combine with regular arguments
def greet(greeting, *names):
    for name in names:
        print(f"{greeting}, {name}!")

greet("Hello", "Alice", "Bob", "Charlie")
# Output:
# Hello, Alice!
# Hello, Bob!
# Hello, Charlie!
```

## The ** Operator (Dictionary Unpacking)

The `**` operator unpacks dictionaries into keyword arguments.

```python
# Unpack dictionary as keyword arguments
def create_person(name, age, city):
    return f"{name} is {age} years old and lives in {city}"

person_info = {"name": "Alice", "age": 25, "city": "NYC"}
result = create_person(**person_info)  # Same as create_person(name="Alice", age=25, city="NYC")
print(result)  # "Alice is 25 years old and lives in NYC"

# Combine with regular arguments
def greet_with_info(greeting, **info):
    print(f"{greeting}!")
    for key, value in info.items():
        print(f"  {key}: {value}")

greet_with_info("Welcome", name="Bob", age=30, city="LA")
# Output:
# Welcome!
#   name: Bob
#   age: 30
#   city: LA
```

## Combining * and **

```python
# Use both operators together
def flexible_function(*args, **kwargs):
    print(f"Positional arguments: {args}")
    print(f"Keyword arguments: {kwargs}")

# Call with mixed arguments
flexible_function(1, 2, 3, name="Alice", age=25)
# Output:
# Positional arguments: (1, 2, 3)
# Keyword arguments: {'name': 'Alice', 'age': 25}
```

## Key Points

- **zip()**: Combines multiple lists into pairs
- **Unpacking**: Assign multiple values at once
- **Different lengths**: Stops at shortest list
- **Multiple lists**: Can zip more than two
- **Unzipping**: Use `*` to separate back
- **`*` operator**: Unpacks lists/tuples and collects extra items
- **`**` operator**: Unpacks dictionaries into keyword arguments
- **Function calls**: Use `*` and `**` to pass arguments dynamically
