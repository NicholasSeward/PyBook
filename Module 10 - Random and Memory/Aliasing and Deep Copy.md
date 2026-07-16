# Aliasing and Deep Copy

## What is Aliasing?

Aliasing happens when multiple variables point to the same object in memory. Think of it like having two remote controls for the same TV - both control the same device, so changing one affects the other.

## The Problem with Aliasing

When you have aliases, changing one variable affects all the others pointing to the same object. This can cause unexpected bugs in your program.

```python
# Aliasing example
original_list = [1, 2, 3]
alias_list = original_list  # Both point to the same list

print(f"Original: {original_list}")
print(f"Alias: {alias_list}")

# Change the alias
alias_list[0] = 99

print(f"After change:")
print(f"Original: {original_list}")  # Also changed!
print(f"Alias: {alias_list}")
```

## Shallow Copy vs Deep Copy

### Shallow Copy
A shallow copy creates a new object but doesn't copy nested objects. It's like copying a folder - you get a new folder, but the files inside are still the same.

```python
import copy

# Original list with nested objects
original = [1, [2, 3], {'a': 4}]
shallow_copy = copy.copy(original)

# Change nested object
shallow_copy[1][0] = 99

print(f"Original: {original}")      # Nested list changed!
print(f"Shallow copy: {shallow_copy}")
```

### Deep Copy
A deep copy creates a completely independent copy of everything, including all nested objects. It's like making a complete duplicate of the folder and all its contents.

```python
import copy

# Original list with nested objects
original = [1, [2, 3], {'a': 4}]
deep_copy = copy.deepcopy(original)

# Change nested object
deep_copy[1][0] = 99

print(f"Original: {original}")      # Unchanged!
print(f"Deep copy: {deep_copy}")
```

## When to Use Each

Use **shallow copy** when:
- You only need to copy the top level
- Nested objects are simple (numbers, strings)
- You want to share nested objects

Use **deep copy** when:
- You need completely independent copies
- Nested objects are complex (lists, dictionaries)
- You want to avoid any shared references

## Key Points

- **Aliasing** - multiple variables pointing to the same object
- **Shallow copy** - copies top level, shares nested objects
- **Deep copy** - copies everything completely
- **Choose wisely** - pick the right copy method for your needs
