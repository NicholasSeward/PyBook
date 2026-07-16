# Intro to Time and Space Complexity

## What is Complexity?

Complexity measures how much time or memory your program needs as the input size grows. Think of it like planning a party - if you invite 10 people, you might need 1 hour to prepare. But if you invite 100 people, you'll need much more time, not just 10 hours.

## Time Complexity

Time complexity tells us how long an algorithm takes to run as the input size increases. We use "Big O" notation to describe this.

### O(1) - Constant Time
Constant time means the operation takes the same amount of time regardless of input size. It's like checking if a light switch is on - it takes the same time whether you have 1 light or 1000 lights.

```python
# O(1) - Constant time
def get_first_item(items):
    return items[0]  # Always takes the same time

# Examples
numbers = [1, 2, 3, 4, 5]
first = get_first_item(numbers)  # Fast

big_list = list(range(1000000))
first = get_first_item(big_list)  # Still fast!
```

### O(n) - Linear Time
Linear time means the time grows proportionally with the input size. If you double the input, you double the time. It's like reading a book - reading 100 pages takes twice as long as reading 50 pages.

```python
# O(n) - Linear time
def find_item(items, target):
    for item in items:
        if item == target:
            return True
    return False

# Examples
small_list = [1, 2, 3, 4, 5]
found = find_item(small_list, 3)  # Quick

big_list = list(range(1000000))
found = find_item(big_list, 500000)  # Takes much longer
```

### O(log n) - Logarithmic Time
Logarithmic time grows very slowly as input size increases. It's like looking up a word in a dictionary - you don't check every word, you jump to the middle and eliminate half the possibilities each time.

```python
# O(log n) - Logarithmic time (binary search)
def binary_search(items, target):
    left, right = 0, len(items) - 1
    
    while left <= right:
        mid = (left + right) // 2
        if items[mid] == target:
            return mid
        elif items[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1

# Examples
small_list = [1, 2, 3, 4, 5]
found = binary_search(small_list, 3)  # Quick

big_list = list(range(1000000))
found = binary_search(big_list, 500000)  # Still very fast!
```

### O(n²) - Quadratic Time
Quadratic time grows much faster - if you double the input, the time increases by 4 times. It's like shaking hands with everyone at a party - with 10 people you shake 45 hands, but with 20 people you shake 190 hands.

```python
# O(n²) - Quadratic time
def find_duplicates(items):
    duplicates = []
    for i in range(len(items)):
        for j in range(i + 1, len(items)):
            if items[i] == items[j]:
                duplicates.append(items[i])
    return duplicates

# Examples
small_list = [1, 2, 1, 3, 2]
dups = find_duplicates(small_list)  # Quick

big_list = [1] * 10000  # 10000 ones
dups = find_duplicates(big_list)  # Very slow!
```

## Space Complexity

Space complexity measures how much memory your program uses as the input size grows. It follows the same Big O notation.

```python
# O(1) - Constant space
def add_numbers(a, b):
    return a + b  # Only uses a few variables

# O(n) - Linear space
def create_list_copy(items):
    return items.copy()  # Creates new list of same size

# O(n²) - Quadratic space
def create_matrix(n):
    return [[0] * n for _ in range(n)]  # Creates n×n matrix
```

## Why This Matters for Businesses

### The Business Problem
Imagine a company that provides an online service. If their algorithm is O(n²), then:
- 100 users might take 1 second to process
- 1000 users would take 100 seconds (over 1.5 minutes!)
- 10000 users would take 10000 seconds (over 2.5 hours!)

### The Cost of Bad Algorithms
Businesses lose money when:
- **Users wait too long** - they leave and go to competitors
- **Server costs explode** - need more powerful computers
- **Customer support increases** - frustrated users need help
- **Revenue decreases** - slow service drives customers away

### Why O(1) and O(log n) Are Gold
Businesses love constant and logarithmic time because:
- **O(1)**: Whether you have 100 or 1 million users, it's always fast
- **O(log n)**: Even with 1 billion users, it's still very fast
- **Scalable**: Can handle growth without massive cost increases
- **Predictable**: Know exactly how much computing power you need

### Real Examples
- **Google Search**: Must be O(log n) or better to handle billions of searches
- **Social Media**: News feeds must load in constant or logarithmic time
- **E-commerce**: Product searches must be fast regardless of catalog size
- **Banking**: Account lookups must be O(1) for security and speed

## Key Points

- **O(1)**: Constant time - always fast, business gold
- **O(log n)**: Logarithmic time - grows very slowly, excellent for business
- **O(n)**: Linear time - acceptable for most business needs
- **O(n²)**: Quadratic time - avoid in business applications
- **Choose wisely**: Bad algorithms cost businesses money and customers
