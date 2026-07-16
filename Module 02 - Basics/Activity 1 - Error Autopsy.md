# Activity 1: Error Autopsy

**Module:** 02 - Basics  
**Time:** 25 minutes  
**Group size:** 3-4  
**Materials:** Shared folder or LMS with 4 broken `.py` snippets

## Goal

Read tracebacks, name the error type, fix the bug, and teach another group what you found.

## Setup (2 min)

Each group gets a different "patient" program (syntax error, `TypeError`, `NameError`, bad cast, etc.).

## Diagnose (10 min)

For your patient, fill this chart:

| Field | Your answer |
|-------|-------------|
| What line does Python blame? | |
| Error type | |
| Plain-English cause | |
| Minimal fix | |
| How you would prevent it next time | |

Do **not** rewrite the whole program. Change as little as possible.

## Cross-check (8 min)

Groups rotate (or swap patients):

1. Can the new group run the fixed version?
2. Do they agree with the diagnosis?
3. Add one improvement note if needed.

## Share-out (5 min)

Each group gives a 45-second case report to the class:

- Symptom (error name)
- Cause
- Cure

## Instructor notes

- Plant only one bug per file so the autopsy stays focused.
- Ask: "Is this syntax or runtime?" before they dig into details.
- Collect best prevention tips on the board for PEP 8 / casting reminders.
