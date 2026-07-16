# Time Module Basics

## Getting Current Time

The `time` module gives you access to the current time and lets you measure how long things take.

```python
import time

# Get current time as seconds since 1970 (Unix timestamp)
current_time = time.time()
print(f"Current timestamp: {current_time}")

# Get current time in a readable format
readable_time = time.ctime()
print(f"Current time: {readable_time}")
```

## Simple Benchmarking

Benchmarking means measuring how long your code takes to run. This helps you compare different approaches.

```python
import time

# Method 1: Using time.time()
start_time = time.time()

# Code to measure
for i in range(1000000):
    pass  # Do nothing

end_time = time.time()
elapsed = end_time - start_time
print(f"Method 1 took: {elapsed:.4f} seconds")

# Method 2: Using time.perf_counter() (more precise)
start = time.perf_counter()

# Code to measure
for i in range(1000000):
    pass

end = time.perf_counter()
elapsed = end - start
print(f"Method 2 took: {elapsed:.4f} seconds")
```

## Comparing Different Approaches

Let's compare two ways to build a list:

```python
import time

# Approach 1: Using a loop
start = time.perf_counter()
numbers = []
for i in range(100000):
    numbers.append(i)
end = time.perf_counter()
loop_time = end - start

# Approach 2: Using list comprehension
start = time.perf_counter()
numbers = [i for i in range(100000)]
end = time.perf_counter()
comp_time = end - start

print(f"Loop approach: {loop_time:.4f} seconds")
print(f"List comprehension: {comp_time:.4f} seconds")
print(f"List comprehension is {loop_time/comp_time:.1f}x faster!")
```

## Key Points

- **`time.time()`**: Basic timestamp, good for simple timing
- **`time.perf_counter()`**: More precise, better for benchmarking
- **Benchmarking**: Compare different approaches to see which is faster
- **Always measure**: Don't guess which code is faster - test it!
