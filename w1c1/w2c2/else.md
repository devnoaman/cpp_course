```markdown
# C++ Else Statement

The `else` statement is used to execute a block of code when the `if` condition evaluates to `false`.

---

## Syntax
```cpp
if (condition) {
    // Block of code to execute if the condition is true
} else {
    // Block of code to execute if the condition is false
}
```

---

## Example: Using `else` to Handle False Conditions
```cpp
#include <iostream>
using namespace std;

int main() {
    int temperature = 30;

    if (temperature < 20) {
        cout << "It's a cold day.";
    } else {
        cout << "It's a warm day.";
    }

    return 0;
}
```

**Output:**
```
It's a warm day.
```

---

## Explanation
1. The variable `temperature` is set to `30`.
2. The `if` condition checks if `temperature < 20`. This evaluates to `false`.
3. Since the condition is false, the program executes the code inside the `else` block, printing "It's a warm day."

---

## Key Points
- The `else` statement is always optional. You can use just an `if` if no alternative block of code is required.
- The `else` block is executed only when the `if` condition evaluates to `false`.

---
```