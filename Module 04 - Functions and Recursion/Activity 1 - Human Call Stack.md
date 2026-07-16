# Activity 1: Human Call Stack

**Module:** 04 - Functions and Recursion  
**Time:** 20-25 minutes  
**Group size:** Whole class + small huddles  
**Materials:** Sticky notes or index cards; open floor space

## Goal

Act out the call stack so students can see frames push and pop, including a tiny recursive example.

## Setup (3 min)

Volunteer roles:

- `main`
- `helper`
- `leaf` (base case)

Each role gets a "frame card" with local variables.

## Demo 1: Simple chain (7 min)

Script (projected):

```py
def leaf():
    return 1

def helper():
    return leaf() + 1

def main():
    print(helper())

main()
```

Students physically stack (stand in a line or stack cards on the board) as calls happen, then unstack on return. Narrate: "Whose locals are visible right now?"

## Huddle predict (5 min)

In groups of 3, predict the stack depth and return values for:

```py
def countdown(n):
    if n <= 0:
        return
    print(n)
    countdown(n - 1)
```

for `countdown(3)`.

## Live reveal (5 min)

Act it out or step in the debugger/TxtBook. Correct misconceptions (base case, multiple frames of same function).

## Exit check

Draw the stack for `countdown(2)` with frame labels only (no full code).

## Instructor notes

- Keep recursion depth tiny (2-4).
- Optional: show a stack overflow story as caution, not a threat.
