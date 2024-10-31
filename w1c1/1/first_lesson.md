
---

# Lesson: Your First C++ Program

In this lesson, we'll go through the simplest C++ program that prints "Hello World!" to the screen. This is often the first step in learning any programming language.

## Code Example

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello World!";
    return 0;
}
```

### Breakdown of the Code

1. **`#include <iostream>`**:
   - This line tells the compiler to include the Input/Output stream library, which is necessary for using `cout` for output.
   - The `iostream` library provides functionality for input and output operations.

2. **`using namespace std;`**:
   - This line allows us to use all the elements in the `std` namespace without having to prefix them with `std::`.
   - For example, we can use `cout` instead of `std::cout`.

3. **`int main() { ... }`**:
   - This defines the main function, which is the entry point of every C++ program.
   - The program execution starts from the `main` function.

4. **`cout << "Hello World!";`**:
   - This line uses `cout` to output the string "Hello World!" to the console.
   - The `<<` operator is called the insertion operator, which sends the string to the output stream.

5. **`return 0;`**:
   - This line indicates that the program finished successfully. Returning `0` is a convention in C++ to signal successful execution.

### Output

When you run this program, the output will be:

```
Hello World!
```

### Running Your Program

To see this program in action, follow these steps:

1. **Write the Code**: Open a C++ development environment (like Code::Blocks, Visual Studio, or an online compiler) and write the code provided above.
  
2. **Compile**: Compile the program. This step translates your C++ code into machine code that the computer can execute.

3. **Run**: Execute the compiled program. You should see "Hello World!" printed on your screen.

### Understanding the Basics

- **Syntax**: Ensure that you use proper syntax in C++. Each statement ends with a semicolon (`;`), and the program structure must be followed.
- **Comments**: You can add comments to your code using `//` for single-line comments or `/* ... */` for multi-line comments, which helps explain your code to others (or yourself later).

> **Practice**: Modify the program to print your name instead of "Hello World!". For example, change the line to `cout << "Hello, [Your Name]!";`.

### Conclusion

This simple program demonstrates the foundational elements of a C++ program. Understanding how to use `cout` for output is a crucial step as you begin your journey in C++ programming. Happy coding!