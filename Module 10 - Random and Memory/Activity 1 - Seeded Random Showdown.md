# Activity 1: Seeded Random Showdown

**Module:** 10 - Random and Memory  
**Time:** 20-25 minutes  
**Group size:** Pairs  
**Materials:** Laptops

## Goal

See how seeds make randomness reproducible, and when shared seeds help testing.

## Match (8 min)

Both partners run with the same seed and same code:

```py
import random
random.seed(42)
print([random.randint(1, 6) for _ in range(5)])
```

Confirm identical output. Then one partner changes the seed; compare.

## Challenge (10 min)

Design a tiny game moment (damage roll, shuffled playlist of 5 songs, coin flips).  
Partner A implements with a seed. Partner B must reproduce the exact sequence on another machine.

## Share-out (5 min)

When should you seed in production vs in tests/class demos?

## Exit check

"Pseudorandom means ___."

## Instructor notes

- Tie to debugging: flaky tests without seeds.
- Optional: show `random.choice` on a team roster.
