```markdown
# C++ Else If Statement

The `else if` statement is used to test multiple conditions. If the first condition evaluates to `false`, the program will check the next condition.

---

## Syntax
```cpp
if (condition1) {
    // Block of code to execute if condition1 is true
} else if (condition2) {
    // Block of code to execute if condition1 is false and condition2 is true
} else {
    // Block of code to execute if both condition1 and condition2 are false
}
```

---

## Example: Using `else if` to Handle Multiple Conditions
```cpp
#include <iostream>
using namespace std;

int main() {
    int score = 85;

    if (score >= 90) {
        cout << "Grade: A";
    } else if (score >= 75) {
        cout << "Grade: B";
    } else if (score >= 50) {
        cout << "Grade: C";
    } else {
        cout << "Grade: F";
    }

    return 0;
}
```

**Output:**
```
Grade: B
```

---

## Explanation
1. The variable `score` is set to `85`.
2. The `if` condition checks if `score >= 90`. This evaluates to `false`.
3. The first `else if` condition checks if `score >= 75`. This evaluates to `true`, so "Grade: B" is printed.
4. The remaining conditions are skipped once a matching condition is found.

---

## Key Points
- Use `else if` to add more conditions after an initial `if`.
- Only the block of the first matching condition is executed; the rest are ignored.
- The `else` block is optional and serves as a fallback for all unmatched conditions.

---
```