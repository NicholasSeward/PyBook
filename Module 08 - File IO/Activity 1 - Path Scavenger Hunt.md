# Activity 1: Path Scavenger Hunt

**Module:** 08 - File IO  
**Time:** 25 minutes  
**Group size:** Pairs  
**Materials:** Shared practice folder with nested files (or zip handed out)

## Goal

Use path tools to locate files and print selected contents without hard-coding fragile absolute paths.

## Hunt list (15 min)

In the provided folder tree, pairs must:

1. Print the current working directory  
2. Find a file named like `notes.txt` (anywhere under the tree)  
3. Count how many `.txt` files exist  
4. Print the first line of a chosen file  

Prefer `pathlib`. Relative paths beat machine-specific absolutes.

## Stamp check (5 min)

Pairs screenshot or paste outputs into a shared sheet. Instructor spot-checks 2-3.

## Share-out (5 min)

Discuss failures: wrong cwd, forgotten recursion, Windows vs POSIX separators.

## Exit check

"A relative path is safer in class repos because ___."

## Instructor notes

- Pre-build a tiny tree so the hunt is fair offline.
- If environment is browser-only, switch to a TxtBook-friendly file API or a mocked path list.
