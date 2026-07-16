# Activity 2: Decompose the Spec

**Module:** 04 - Functions and Recursion  
**Time:** 25-30 minutes  
**Group size:** 3-4  
**Materials:** Whiteboard / shared doc

## Goal

Turn a messy problem statement into a clean set of function names and responsibilities, then implement only one piece.

## Spec (posted by instructor)

Example:

> Build a mini weather helper. Ask for temperature (F) and whether it is raining (yes/no). Print a clothing suggestion and a one-line summary. Use at least three functions. No giant `main` full of logic.

## Design sprint (10 min)

On the board, list:

| Function | Inputs | Output / effect | Owns which decision? |
|----------|--------|-----------------|----------------------|
| | | | |

Groups may not write full implementations yet.

## Peer critique (5 min)

Rotate to another group's board. Leave two sticky notes:

- Keep: ___
- Change: ___

## Implement one slice (8 min)

Each group fully implements **one** function and stubs the others with `pass` or `TODO`. Run a quick manual test for that slice.

## Share-out (5 min)

Compare interfaces across groups. Vote: clearest decomposition.

## Instructor notes

- Reward boring clear names over clever ones.
- Call out hidden coupling ("this function secretly prints and returns").
