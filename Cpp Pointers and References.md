# C++ Pointers and References

Keep it simple: what `*` and `&` mean before and after things.

## Core ideas

| Where you see it | Meaning |
|------------------|---------|
| `&` in an **expression** | address-of (gets a pointer to something) |
| `*` in a **declaration** | pointer type |
| `*` in an **expression** | dereference (go to the pointed-to value) |
| `&` in a **declaration** | reference type (an alias) |

```cpp
int x = 10;
int* p = &x;   // & in expression: address-of; * in declaration: pointer to int
*p = 20;       // * in expression: write through the pointer
int& r = x;    // & in declaration: r refers to x
```

- `int* p;` means "p is a pointer to int"
- `*p = 20;` writes to what `p` points to
- `int& r = x;` means "r refers to x"

## Pointer vs reference

- A **pointer** can be null (`nullptr`) and reseated; use `*` to dereference.
- A **reference** must bind to a valid object and cannot be reseated.

```cpp
void incPtr(int* p) { if (p) (*p)++; }
void incRef(int& r) { r++; }
```

## Null pointer

```cpp
int* p = nullptr;
if (p != nullptr) {
    // safe to use *p
}
```

Pointers often come from arrays or containers:

```cpp
#include <vector>

std::vector<int> v{1, 2, 3};
int* pv = v.data();        // or &v[0] if v is not empty
```

## Style note

Both of these compile the same. Pick one style and stay consistent:

```cpp
int* p;   int& r = x;
int *p;   int &r = x;
```

## Tiny example

```cpp
#include <iostream>

void incPtr(int* p)  { if (p) (*p)++; }
void incRef(int& r)  { r++; }

int main() {
    int x = 10;
    int* p = &x;    // address-of
    int& r = x;     // reference to x

    *p = 20;        // dereference and write
    incPtr(p);      // x becomes 21
    incRef(r);      // x becomes 22

    std::cout << x << "\n";  // 22
    return 0;
}
```

## Try it now

**Prompt:** Write a function `void doubleIt(int& n)` that doubles `n` through a reference. In `main`, set `x = 5`, call `doubleIt(x)`, and print `x` (should be `10`).

```cpp
#include <iostream>

// TODO: write doubleIt

int main() {
    int x = 5;
    // TODO: call doubleIt and print x
    return 0;
}
```

:::details Hint

The parameter is `int&`, so assign with `n = n * 2` (no `*` needed).

:::

:::details Solution

**Reasoning:** A reference is an alias, so updates to `n` update the caller's `x`.

```cpp
#include <iostream>

void doubleIt(int& n) {
    n = n * 2;
}

int main() {
    int x = 5;
    doubleIt(x);
    std::cout << x << "\n";  // 10
    return 0;
}
```

:::
