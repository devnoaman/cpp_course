```markdown
# C++ Functions

Functions are blocks of code that perform specific tasks. They help make programs more modular, reusable, and easier to understand.

## Defining a Function

To define a function, specify its return type, name, and parameters (if any). Then write the code inside `{}` braces.

### Syntax
```cpp
return_type functionName(parameters) {
    // code to be executed
    return value; // only if the return_type is not void
}
```

### Example: Defining and Calling a Function

```cpp
#include <iostream>
using namespace std;

// Define a function that adds two numbers
int add(int x, int y) {
    return x + y;
}

int main() {
    int result = add(5, 3);
    cout << "Sum: " << result;
    return 0;
}
```

Output:
```
Sum: 8
```

In this example:
- `add` is a function that takes two integers (`x` and `y`) and returns their sum.
- We call `add(5, 3)` in `main()` and store the result in `result`.

---

## Function Parameters

Parameters are variables listed in the function definition. They allow you to pass values to the function when calling it.

### Example: Function with Parameters
```cpp
#include <iostream>
using namespace std;

void greet(string name) {
    cout << "Hello, " << name << "!";
}

int main() {
    greet("Alice");
    return 0;
}
```

Output:
```
Hello, Alice!
```

Here, `greet` takes a `string` parameter and prints a personalized greeting.

---

## Default Parameters

You can set default values for parameters, so if no argument is provided, the default value is used.

### Example
```cpp
#include <iostream>
using namespace std;

void introduce(string name = "Guest") {
    cout << "Hello, " << name << "!";
}

int main() {
    introduce();        // Uses default parameter
    introduce("Bob");   // Uses provided argument
    return 0;
}
```

Output:
```
Hello, Guest!
Hello, Bob!
```

---

## Function Overloading

C++ allows multiple functions with the same name but different parameter types or counts. This is known as function overloading.

### Example
```cpp
#include <iostream>
using namespace std;

int add(int x, int y) {
    return x + y;
}

double add(double x, double y) {
    return x + y;
}

int main() {
    cout << add(5, 3) << "\n";       // Calls int version
    cout << add(5.5, 3.2) << "\n";   // Calls double version
    return 0;
}
```

Output:
```
8
8.7
```

Here, `add` is overloaded to handle both `int` and `double` parameters.

---

## Recursion

A function can call itself. This technique is called recursion and is often used to solve problems that can be broken down into smaller, similar problems.

### Example: Factorial Using Recursion
```cpp
#include <iostream>
using namespace std;

int factorial(int n) {
    if (n <= 1) return 1;
    return n * factorial(n - 1);
}

int main() {
    cout << "Factorial of 5: " << factorial(5);
    return 0;
}
```

Output:
```
Factorial of 5: 120
```

In this example, `factorial` calls itself with `n - 1` until `n` is 1.

---

## Summary

- **Defining Functions**: Use `return_type functionName(parameters) {}`.
- **Function Parameters**: Pass values into functions.
- **Default Parameters**: Set default values for parameters.
- **Function Overloading**: Define multiple functions with the same name but different parameter types.
- **Recursion**: A function calling itself to solve a problem.

---
```
```