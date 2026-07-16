# Activity 2: Broken File Clinic

**Module:** 08 - File IO  
**Time:** 25-30 minutes  
**Group size:** 3-4  
**Materials:** 3 planted broken scripts (bad mode, missing close/context manager, bare open without try)

## Goal

Fix real I/O bugs and explain the failure mode to another group.

## Clinic flow (18 min)

Each group receives one broken script first, then rotates:

| Bug type | What to restore |
|----------|-----------------|
| Wrong mode | Read vs write vs append |
| No error handling | `try/except` around missing file |
| Resource handling | Prefer `with open(...)` |

Document before/after in 4 bullets.

## Teach-back (7 min)

Groups teach their final case to neighbors in 90 seconds.

## Exit check

When do you want `with open` even for a "tiny" script?

## Instructor notes

- Keep files short (15 lines).
- Remind: fixing by deleting the feature does not count.
