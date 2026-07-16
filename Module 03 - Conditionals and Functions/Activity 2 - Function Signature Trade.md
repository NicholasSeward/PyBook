# Activity 2: Function Signature Trade

**Module:** 03 - Conditionals and Functions  
**Time:** 25-30 minutes  
**Group size:** Pairs  
**Materials:** Laptops or paper

## Goal

Separate **interface** from **implementation**: one partner designs a function header and docstring; the other implements it; then swap.

## Round 1 (10 min)

**Partner A** writes only:

- function name
- parameters
- docstring (what it returns / side effects)
- 2 example calls with expected results

**Partner B** implements the body to match. No changing the signature without negotiating.

## Round 2 (10 min)

Swap roles with a new mini-spec (instructor can provide prompts):

- `letter_grade(score) -> str`
- `is_weekend(day_name) -> bool`
- `max_of_three(a, b, c) -> number`
- `describe_temp(f) -> str` using `if/elif/else`

## Share-out (5-8 min)

Two pairs show:

1. A signature that made implementation easy
2. A signature that was ambiguous (and how they fixed the docstring)

## Exit check

Write one sentence: "A good function signature tells the caller ___."

## Instructor notes

- Ban globals for this activity.
- If conflict appears, coach negotiation: rename params, add a return note, add a precondition.
