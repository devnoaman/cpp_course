```markdown
# C++ Do/While Loop

## Overview
The `do/while` loop is a variant of the `while` loop. It guarantees that the code block executes **at least once**, as the condition is checked **after** the code block runs.

---

## Syntax

```cpp
do {
    // Code block to be executed
} while (condition);
```

---

## Example: Basic Do/While Loop

The following example demonstrates a `do/while` loop that prints numbers from 0 to 4:

```cpp
#include <iostream>
using namespace std;

int main() {
    int i = 0;

    do {
        cout << i << "\n"; // Print the current value of i
        i++;               // Increment i
    } while (i < 5);

    return 0;
}
// Output:
// 0
// 1
// 2
// 3
// 4
```

---

## Key Points
1. **Execution Guarantee**:
   - The code block is executed **once** before the condition is evaluated, even if the condition is `false` initially.

2. **Condition Check**:
   - The condition is checked **after** the execution of the code block.

3. **Use Case**:
   - Ideal for scenarios where the loop must run at least once (e.g., menu prompts or input validation).

---

## Practical Example: User Input Validation

This example ensures the user enters a positive number:

```cpp
#include <iostream>
using namespace std;

int main() {
    int number;

    do {
        cout << "Enter a positive number: ";
        cin >> number;

        if (number < 0) {
            cout << "Invalid input. Try again.\n";
        }
    } while (number < 0);

    cout << "You entered: " << number << endl;

    return 0;
}
// Sample Input:
// -3
// -1
// 5
// Output:
// Enter a positive number: -3
// Invalid input. Try again.
// Enter a positive number: -1
// Invalid input. Try again.
// Enter a positive number: 5
// You entered: 5
```

---

## Comparison: `while` vs. `do/while`

| Feature               | `while` Loop               | `do/while` Loop          |
|-----------------------|----------------------------|--------------------------|
| **Condition Check**    | Before the code block runs | After the code block runs |
| **Guaranteed Execution** | No, may not run at all     | Yes, runs at least once   |
| **Typical Use Case**    | When execution depends on condition | When at least one execution is needed |

---
```