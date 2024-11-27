```markdown
# C++ If ... Else

C++ allows you to execute specific blocks of code based on certain conditions using conditional statements. These statements evaluate logical conditions and decide the flow of execution.

---

## Logical Conditions
C++ supports the following logical conditions:
- **Less than**: `a < b`
- **Less than or equal to**: `a <= b`
- **Greater than**: `a > b`
- **Greater than or equal to**: `a >= b`
- **Equal to**: `a == b`
- **Not equal to**: `a != b`

---

## Conditional Statements in C++
- **`if`**: Executes a block of code if the condition is true.
- **`else`**: Executes a block of code if the `if` condition is false.
- **`else if`**: Tests another condition if the previous `if` condition is false.
- **`switch`**: Specifies multiple alternative blocks of code to execute.

---

## The `if` Statement

The `if` statement executes a block of code only if the condition evaluates to true.

### Syntax
```cpp
if (condition) {
    // Block of code to execute if the condition is true
}
```

### Example: Using `if` to Check a Condition
```cpp
#include <iostream>
using namespace std;

int main() {
    int age = 20;

    if (age >= 18) {
        cout << "You are an adult.";
    }

    return 0;
}
```

**Output:**
```
You are an adult.
```

In this example, the condition `age >= 18` is true, so the message is printed.

---

## The `else` Statement

Use the `else` statement to specify what should happen if the `if` condition is false.

### Syntax
```cpp
if (condition) {
    // Block of code to execute if the condition is true
} else {
    // Block of code to execute if the condition is false
}
```

### Example: Using `if` and `else`
```cpp
#include <iostream>
using namespace std;

int main() {
    int age = 16;

    if (age >= 18) {
        cout << "You are an adult.";
    } else {
        cout << "You are a minor.";
    }

    return 0;
}
```

**Output:**
```
You are a minor.
```

Here, the condition `age >= 18` is false, so the code inside the `else` block executes.

---

## The `else if` Statement

Use `else if` to check another condition when the `if` condition is false.

### Syntax
```cpp
if (condition1) {
    // Block of code to execute if condition1 is true
} else if (condition2) {
    // Block of code to execute if condition2 is true
} else {
    // Block of code to execute if both condition1 and condition2 are false
}
```

### Example: Using `else if`
```cpp
#include <iostream>
using namespace std;

int main() {
    int score = 75;

    if (score >= 90) {
        cout << "Grade: A";
    } else if (score >= 80) {
        cout << "Grade: B";
    } else if (score >= 70) {
        cout << "Grade: C";
    } else {
        cout << "Grade: F";
    }

    return 0;
}
```

**Output:**
```
Grade: C
```

Here, the program evaluates the conditions in order. Since `score >= 70` is true, the corresponding block is executed.

---

## Example: Testing Variables
You can also use variables to test conditions:

```cpp
#include <iostream>
using namespace std;

int main() {
    int temperature = 30;

    if (temperature > 25) {
        cout << "It's a hot day!";
    } else {
        cout << "It's a cool day!";
    }

    return 0;
}
```

**Output:**
```
It's a hot day!
```

---

## Key Points
1. **Conditions**:
   - Logical operators are used to compare values.
   - Conditions evaluate to `true` or `false`.

2. **Flow Control**:
   - `if` runs code when a condition is true.
   - `else` runs code when the condition is false.
   - `else if` adds additional conditional checks.

3. **Readability**:
   - Proper indentation improves readability and maintainability.

---
```