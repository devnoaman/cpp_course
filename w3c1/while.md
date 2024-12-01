```markdown
# C++ While Loop

## Overview
A `while` loop executes a block of code as long as the specified condition evaluates to `true`. It is particularly useful when the number of iterations is unknown in advance.

---

## Syntax

```cpp
while (condition) {
  // Code block to be executed
}
```

---

## Example: Simple While Loop

The following example demonstrates a `while` loop that prints numbers from 0 to 4:

```cpp
#include <iostream>
using namespace std;

int main() {
    int i = 0;

    while (i < 5) {
        cout << i << "\n"; // Print the current value of i
        i++;               // Increment i to avoid an infinite loop
    }

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
1. **Condition Check**:
   - The loop condition is checked **before** the code block executes.
   - If the condition is `false` initially, the loop will not execute at all.

2. **Avoid Infinite Loops**:
   - Ensure the loop variable is modified within the loop; otherwise, the loop may run indefinitely.

   Example of an infinite loop:
   ```cpp
   int i = 0;
   while (i < 5) {
       cout << i << "\n";
       // Missing i++;
   }
   ```

3. **Applications**:
   - Useful when the number of iterations is not predetermined (e.g., reading user input until a specific condition is met).

---

## Practical Example: Sum of Numbers

This example calculates the sum of numbers from 1 to `n` using a `while` loop:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n, sum = 0, i = 1;

    cout << "Enter a positive number: ";
    cin >> n;

    while (i <= n) {
        sum += i; // Add current i to sum
        i++;      // Increment i
    }

    cout << "Sum of numbers from 1 to " << n << " is: " << sum << endl;

    return 0;
}
// Input: 5
// Output: Sum of numbers from 1 to 5 is: 15
```

---
```