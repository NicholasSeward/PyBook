# Algorithm Analysis

## Why Analyze Algorithms?

Understanding algorithm performance helps you choose the right tool for the job. A fast algorithm can save hours of waiting time and thousands of dollars in server costs.

## Sorting Algorithms

### Bubble Sort - O(n²)
**How it works**: Compare adjacent items and swap if they're in wrong order.

**Performance**:
- 100 items: 10,000 operations
- 1,000 items: 1 million operations
- 10,000 items: 100 million operations

**When to use**: Never! Always use built-in sort functions.

**Real example**: Python's `.sort()` and `sorted()` are much faster.

### Merge Sort - O(n × log n)
**How it works**: Split list in half, sort each half, merge them together.

**Performance**:
- 100 items: 664 operations
- 1,000 items: 9,966 operations
- 10,000 items: 132,877 operations

**When to use**: When you need guaranteed performance or are learning.

**Real example**: Python's built-in sort uses a hybrid approach.

### Quick Sort - O(n × log n) average, O(n²) worst
**How it works**: Pick a "pivot" element, partition around it, repeat.

**Performance**:
- Usually O(n × log n) - very fast
- Worst case O(n²) - but rare with good pivot choice

**When to use**: Often the fastest in practice, used in many languages.

**Real example**: Python's built-in sort, many database systems.

## Search Algorithms

### Linear Search - O(n)
**How it works**: Check each item one by one until you find it.

**Performance**:
- 100 items: up to 100 checks
- 1,000 items: up to 1,000 checks
- 1,000,000 items: up to 1,000,000 checks

**When to use**: Small lists, unsorted data, simple implementation.

**Real example**: Finding a name in a short contact list.

### Binary Search - O(log n)
**How it works**: Look at middle item, eliminate half, repeat.

**Performance**:
- 100 items: up to 7 checks
- 1,000 items: up to 10 checks
- 1,000,000 items: up to 20 checks

**When to use**: Sorted data, large lists, need for speed.

**Real example**: Looking up words in a dictionary, finding files.

## Performance Comparison

### Small Lists (100 items)
- **Bubble Sort**: 10,000 operations (slow)
- **Merge Sort**: 664 operations (fast)
- **Linear Search**: 100 operations max
- **Binary Search**: 7 operations max

### Large Lists (1,000,000 items)
- **Bubble Sort**: 1 trillion operations (impossible)
- **Merge Sort**: 19.9 million operations (reasonable)
- **Linear Search**: 1 million operations max (slow)
- **Binary Search**: 20 operations max (lightning fast)

## Business Impact

### The Cost of Bad Algorithms
**Company with 1 million customers**:
- **Bad algorithm (O(n²))**: Customers wait hours, leave for competitors
- **Good algorithm (O(n × log n))**: Customers get results in seconds, stay loyal

**Server costs**:
- **O(n²)**: Need expensive supercomputers
- **O(n × log n)**: Regular servers work fine
- **O(log n)**: Even cheap servers are fast

### Real-World Examples
- **Google Search**: Must be O(log n) or better
- **Amazon**: Product search uses sophisticated algorithms
- **Netflix**: Movie recommendations use O(n × log n) algorithms
- **Banks**: Fraud detection must be fast (O(n) or better)

## Key Points

- **Sorting**: Built-in sorts are O(n × log n) - use them!
- **Searching**: Binary search is O(log n) - amazing for large data
- **Performance matters**: Bad algorithms cost money and customers
- **Know your Big O**: Choose algorithms that scale with your business
- **Built-in functions**: Often the fastest and most reliable option
- **Business impact**: Algorithm choice affects customer satisfaction and costs
