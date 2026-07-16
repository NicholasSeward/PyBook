# Compiled vs Interpreted

Programming languages can generally be divided into compiled and interpreted languages. The difference lies in how the code you write is turned into instructions a computer can run.

## Compiled Languages

In a compiled language, your source code is translated all at once into machine code (binary instructions the CPU can run directly). This happens before the program runs, using a special program called a compiler. The result is usually an executable file.

**Examples:** C, C++, Rust, Go, Swift

**Pros:**
- Programs usually run faster, since they are already in machine code
- Compiler can catch many errors before the program is run
- Often better performance for large, complex applications

**Cons:**
- Must recompile after every change, which can slow development
- The compiled program is specific to one operating system or CPU architecture (e.g., Windows vs. macOS)

## Interpreted Languages

In an interpreted language, the source code is read and executed line by line by another program called an interpreter. Instead of producing an executable file, the interpreter translates and runs the code as the program runs.

**Examples:** Python, JavaScript, Ruby, PHP

**Pros:**
- Easier to test and modify—just run the code directly
- Often better for beginners because there's no compilation step
- Portable across different systems, as long as an interpreter is available

**Cons:**
- Slower execution speed compared to compiled code
- Errors may only show up when the program reaches that part of the code

## A Middle Ground

Some languages combine these approaches. For example:

- **Java and C#** compile source code into bytecode, which is not raw machine code.
- This bytecode runs on a virtual machine (like the Java Virtual Machine), which interprets or just-in-time (JIT) compiles it during execution.
- This gives some of the efficiency of compiled languages with some of the flexibility of interpreted ones.
