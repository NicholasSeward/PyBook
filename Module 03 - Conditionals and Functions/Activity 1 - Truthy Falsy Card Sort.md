# Activity 1: Truthy / Falsy Card Sort

**Module:** 03 - Conditionals and Functions  
**Time:** 20-25 minutes  
**Group size:** 3-4  
**Materials:** Printed/digital cards with values like `0`, `""`, `"0"`, `[]`, `[0]`, `None`, `False`, `1`, `"False"`

## Goal

Sort values into **Truthy** vs **Falsy**, then write an `if` that uses one surprising case correctly.

## Sort (8 min)

As a team, place each card in Truthy or Falsy. No running code yet.

Disputed cards go in a middle "argue later" pile.

## Verify (7 min)

Run quick checks in Python:

```py
print(bool(VALUE))
```

Fix the board. For each surprise, write one plain sentence ("Empty list is falsy because...").

## Apply (5 min)

Each team writes one small snippet that depends on truthiness, for example:

```py
items = []
if items:
    print("has items")
else:
    print("empty")
```

## Share-out (5 min)

Teams share one surprising value and their snippet. Class votes: clear or sneaky?

## Instructor notes

- Emphasize: prefer explicit checks (`if items:` vs `if len(items) != 0`) with intent.
- Call out that `"False"` is truthy (non-empty string).
