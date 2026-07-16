# Number Systems

When we work with numbers in programming, it's important to understand that computers don't just use the familiar decimal system (base 10). They rely heavily on binary (base 2) and often use hexadecimal (base 16) as a shorthand.

## Decimal (Base 10)

This is the system you already know: digits go from 0 to 9, and each column represents a power of 10.

**Example:**

```
374 = (3 × 10²) + (7 × 10¹) + (4 × 10⁰)
    = 300 + 70 + 4
```

## Binary (Base 2)

Binary only uses two digits: 0 and 1. Each column represents a power of 2 instead of 10.

**Example:**

```
1011₂ = (1 × 2³) + (0 × 2²) + (1 × 2¹) + (1 × 2⁰)
      = 8 + 0 + 2 + 1
      = 11 in decimal
```

Notice the column values:

- Rightmost column = 2⁰ = 1
- Next column = 2¹ = 2
- Next = 2² = 4
- Next = 2³ = 8
- Then 16, 32, 64, …

This is why binary is so important: every bit (binary digit) can only be 0 or 1, and combining them in columns lets us represent any number.

A group of 8 bits is called a **byte**. For example, a byte can represent numbers from 0 to 255 in binary.

## Hexadecimal (Base 16)

Hexadecimal uses 16 symbols:

```
0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F
```

(where A = 10, B = 11, … F = 15 in decimal).

Each column represents a power of 16.

**Example:**

```
2F₁₆ = (2 × 16¹) + (15 × 16⁰)
     = 32 + 15
     = 47 in decimal
```

Why use hex? Because one hex digit exactly represents 4 bits (half a byte or a **nibble**). So two hex digits represent one full byte.

**Example:** FF₁₆ = 11111111₂ = 255₁₀

This makes hex an efficient shorthand for binary.

## Conversions

### Decimal → Binary

Repeatedly divide the decimal number by 2, keeping track of the remainders. Read remainders from bottom to top.

**Example: Convert 13 → binary**
```
13 ÷ 2 = 6 remainder 1
6 ÷ 2 = 3 remainder 0
3 ÷ 2 = 1 remainder 1
1 ÷ 2 = 0 remainder 1
→ 13 = 1101₂
```

### Binary → Decimal

Multiply each binary digit by its column value (powers of 2).

**Example:** 1101₂ = (1×8) + (1×4) + (0×2) + (1×1) = 13₁₀

### Hex → Binary

Convert each hex digit into its 4-bit binary equivalent.

**Example:** 2F₁₆ = 0010 1111₂

### Binary → Hex

Group binary digits into chunks of 4 (from right to left), then convert each group.

**Example:** 101111₂ = 0010 1111₂ = 2F₁₆

## Why This Matters

- **Binary** is how all data is stored in a computer (because of bits and bytes).
- **Hexadecimal** is used as a compact, human-readable shorthand for binary, especially in memory addresses, color codes, and debugging.
- **Decimal** is what we use in everyday life, but under the hood, your computer is running in binary.

## Practice Links

- **Binary/Decimal/Hex Converter (interactive)**: https://www.rapidtables.com/convert/number/index.html
- **Practice Binary Numbers Game**: https://games.penjee.com/binary-numbers-game/
- **Number System Practice Problems**: https://www.geeksforgeeks.org/number-system-and-base-conversions/
- **Hexadecimal Bee Game**: https://www.wisc-online.com/arcade/games/computer-science/foundational-it-skills/2169/hexadecimal-bee-game
