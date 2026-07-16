# Activity 2: Mutation Mystery

**Module:** 06 - Data Structures  
**Time:** 20-25 minutes  
**Group size:** Pairs  
**Materials:** Laptops; projector

## Goal

Predict aliasing outcomes before running code, then reconcile with reality.

## Mysteries (12 min)

For each snippet, pairs write **Predicted final values** before running.

### Mystery A

```py
a = [1, 2, 3]
b = a
b.append(4)
print(a)
print(b)
```

### Mystery B

```py
a = [1, 2, 3]
b = a.copy()
b.append(4)
print(a)
print(b)
```

### Mystery C

```py
grades = {"Ada": 90}
backup = grades
backup["Ada"] = 100
print(grades)
```

## Reveal (5 min)

Run live. Update predictions. Draw a quick reference diagram for A vs B.

## Share-out (5 min)

Pairs invent a one-line rule for teammates: "Assignment of a list copies the ___, not the ___."

## Instructor notes

- If advanced: show shallow copy pitfall with nested lists (optional stretch).
- Connect to why functions should avoid surprising mutation of caller data.
