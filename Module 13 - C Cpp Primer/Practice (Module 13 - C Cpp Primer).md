# Practice Assignment: Module 13 - C/C++ Primer

## Overview
Complete 1 problem total  -  choose either the Triangle (Section 1) or Hi-Lo (Section 2). Each reinforces core C++ basics (I/O, loops, randomness/control flow).

## Instructions
- Choose 1 problem (either Section 1 or Section 2)
- Use clear, readable code and standard C++17
- Test your code with different inputs
- In GitHub Codespaces, you do NOT need bash commands  -  open your file and press the Run button (or Run → Run Without Debugging) to build and run the active C++ file

## Build and Run
- In GitHub Codespaces: open your C++ file and press the Run button; it will compile and run the active file.

## File Naming and Submission

### File Naming
Pick ONE of the following filenames based on the problem you choose:
- Problem 1a: `program1a.cpp` (Triangle of Stars)
- Problem 2a: `program2a.cpp` (Hi-Lo Guessing Game)

### AI Disclaimer
Each file must include an AI Disclaimer at the top.

### Submission Process
1. Create your program files
2. Test your code thoroughly
3. Commit and push to GitHub
4. Submit your repository URL

Example repository URL: `https://github.com/Seward-Classes/practice-13-username`

---

## Section 1: Basics and I/O (Choose 1)

### 1a: Triangle of Stars

File: `program1a.cpp`

Write a program that asks for a positive integer `n` and prints a left-aligned triangle of `*` of height `n`.

Requirements:
- Prompt the user: "Enter a positive integer: " and read `n`
- If `n <= 0`, you may print an error and exit (optional)
- Print `n` lines; line i contains i stars

Your program should produce this output (for n = 4):
```
Enter a positive integer: 4
*
**
***
****
```

Starter code:
```cpp
#include <iostream>

int main() {
    std::cout << "Enter a positive integer: ";
    int n{};
    std::cin >> n;

    // TODO: Validate n > 0 (optional)

    // TODO: Print a left-aligned triangle of height n.
    // Hint: Use two nested for-loops:
    //   - outer loop controls the number of rows (1..n)
    //   - inner loop prints the right number of '*' for that row

    return 0;
}
```

---

## Section 2: Randomness and Control Flow (Choose 1)

### 2a: Hi-Lo Guessing Game (Mersenne Twister)

File: `program2a.cpp`

The program picks a secret number in [1, 100]. After each user guess, print "Too low", "Too high", or "You got it!". Continue until correct.

Requirements:
- Use `std::random_device`, `std::mt19937`, and `std::uniform_int_distribution<int>` to generate the secret
- Prompt for guesses in a loop
- Validate input is an integer; if not, clear and retry
- End when the user guesses correctly

Example session (secret unknown to player):
```
I'm thinking of a number between 1 and 100. Try to guess it!
Enter your guess: 20
Too low
Enter your guess: 90
Too high
Enter your guess: 65
You got it!
```

Starter code:
```cpp
#include <iostream>
#include <random>

int main() {
    // Generate secret number in [1, 100]
    std::random_device rd;
    std::mt19937 gen(rd());
    std::uniform_int_distribution<int> dist(1, 100);
    int secret = dist(gen);

    // TODO: Prompt user and play Hi-Lo guessing game
    // - Prompt for guesses in a loop
    // - Validate input is an integer; if not, clear and retry
    // - After each guess, print "Too low", "Too high", or "You got it!"
    // - Continue until the user guesses correctly

    return 0;
}
```

Hints:
- Use `if (guess < secret)`, `else if (guess > secret)`, `else`
- To limit attempts, add a counter and break after N tries
- For replay, wrap logic in a loop and regenerate `secret`

---

## Submission Checklist
- [ ] Completed ONE problem (Triangle OR Hi-Lo)
- [ ] Files are named correctly (`program1a.cpp`, `program2a.cpp`)
- [ ] Each file includes an AI Disclaimer at the top
- [ ] Tested with multiple inputs and edge cases
- [ ] All files committed and pushed to GitHub
- [ ] Repository URL submitted on BlackBoard 

