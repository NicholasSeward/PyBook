# Activity 1: Python to C++ Translation Relay

**Module:** 13 - C C++ Primer  
**Time:** 25-30 minutes  
**Group size:** 3-4  
**Materials:** Laptops with C++ toolchain or Codespaces

## Goal

Translate a tiny Python snippet into C++ as a team, noticing types, braces, and compile steps.

## Source Python (example)

```py
def main():
    n = int(input("n: "))
    total = 0
    for i in range(n):
        total += i
    print(total)

main()
```

## Relay (15 min)

Roles:

1. Declare types / includes  
2. Write loop  
3. Compile and fix first errors  
4. Run and verify against Python output  

## Share-out (8 min)

Each group reports one compile error they hit and the fix (missing `;`, wrong type, `<<` vs `print`).

## Exit check

"C++ made me declare ___ that Python inferred."

## Instructor notes

- Prefer a known-good Codespace image.
- Keep I/O minimal; focus on types and compile cycle.
