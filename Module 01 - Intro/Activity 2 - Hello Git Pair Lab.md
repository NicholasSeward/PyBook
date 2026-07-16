# Activity 2: Hello Git Pair Lab

**Module:** 01 - Intro  
**Time:** 25-30 minutes  
**Group size:** Pairs  
**Materials:** Laptops; GitHub access; projector for one demo pair

## Goal

Create a tiny Python file together, commit it, and push so both partners see the shared repo workflow.

## Setup (3 min)

1. Pair up (driver + navigator). Switch roles halfway.
2. One partner creates or opens the course practice repo (instructor specifies which).
3. Confirm both can pull/clone successfully.

## Part A: Write together (8 min)

In `hello_pair.py` (or instructor-provided filename):

```py
# Authors: <name1>, <name2>
print("Hello from our pair!")
print("We can run Python and use Git.")
```

Run it. Fix any path/IDE issues as a pair before moving on.

## Part B: First commit (8 min)

Driver runs (or uses GUI equivalent):

1. `git status`
2. `git add` the file
3. `git commit -m "Add pair hello program"`
4. `git push`

Navigator narrates what each step means.

## Part C: Role switch + verify (6 min)

Switch roles. Second partner:

1. Pull latest
2. Change the second print message
3. Commit and push again

## Share-out (5 min)

2-3 pairs show:

- Their commit history (one meaningful message)
- One mistake they hit (auth, wrong folder, untracked file) and the fix

## Exit check

Each student pastes their repo URL (or commit hash) in the course chat / sheet.

## Instructor notes

- Pre-flight: auth (HTTPS token or SSH) is the usual blocker. Have a help station.
- If time is short, skip the second push and stop after one successful push.
- Celebrate "fixed a real Git error" as much as clean runs.
