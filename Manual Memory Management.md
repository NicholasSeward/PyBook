# Manual Memory Management

## Python vs C++ Memory

### Python: Automatic Garbage Collection
Python automatically manages memory for you:
- Objects are created when you need them
- Memory is freed when objects are no longer used
- You never think about memory management
- Slower but safer

```python
# Python - memory management is automatic
def create_list():
    my_list = [1, 2, 3, 4, 5]  # Memory allocated
    return my_list

result = create_list()
# When result goes out of scope, Python frees the memory automatically
```

### C++: Manual Memory Management
In C++, you must manage memory yourself:
- You allocate memory when you need it
- You must free memory when you're done
- Faster but more dangerous
- Memory leaks can crash your program

```cpp
// C++ - you must manage memory manually
std::vector<int> create_vector() {
    std::vector<int> vec = {1, 2, 3, 4, 5};  // STL vector
    return vec;
}

std::vector<int> result = create_vector();
// Use the vector...
// No need to delete - STL vector manages memory automatically!
```

## Stack vs Heap

### Stack Variables (Automatic)
Variables on the stack are automatically managed:
- Created when function starts
- Deleted when function ends
- Fast and safe
- Limited size

```cpp
void function() {
    int x = 5;        // Stack variable - auto-deleted
    double y = 3.14;  // Stack variable - auto-deleted
    // When function ends, x and y are automatically deleted
}
```

### Heap Variables (Manual)
Variables on the heap must be manually managed:
- Created with `new`
- Must be deleted with `delete`
- Can be any size
- Can cause memory leaks

```cpp
void function() {
    int* x = new int(5);        // Heap variable - must delete
    double* y = new double(3.14); // Heap variable - must delete
    
    // Use x and y...
    
    delete x;  // Must delete manually
    delete y;  // Must delete manually
}
```

## Common Memory Problems

### Memory Leaks
Forgetting to delete memory (with raw pointers):
```cpp
void bad_function() {
    int* arr = new int[1000];  // Allocate memory
    // Use array...
    // Forgot to delete! Memory leak!
}
// Better: Use STL vector instead
void good_function() {
    std::vector<int> vec(1000);  // No memory leak possible
    // Use vector...
    // Automatically cleaned up!
}
```

### Double Deletion
Deleting the same memory twice:
```cpp
int* ptr = new int(42);
delete ptr;   // OK
delete ptr;   // ERROR! Already deleted
```

### Dangling Pointers
Using memory after it's deleted:
```cpp
int* ptr = new int(42);
delete ptr;   // Memory freed
*ptr = 100;   // ERROR! Using freed memory
```

## Smart Pointers (Modern C++)

Modern C++ has smart pointers that help:
```cpp
#include <memory>

void smart_function() {
    auto ptr = std::make_unique<int>(42);  // Automatically deleted
    // No need to delete - it's automatic!
}
```

## Key Points

- **Python**: Automatic garbage collection, safer, slower
- **C++**: Manual memory management, faster, more dangerous
- **Stack**: Automatic cleanup, fast, limited size
- **Heap**: Manual cleanup, flexible size, can leak
- **STL containers**: Vectors, strings, etc. manage memory automatically
- **Smart pointers**: Modern C++ solution for safer memory
- **Memory leaks**: Common with raw pointers - use STL containers when possible
