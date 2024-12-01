```markdown
# C++ `break` and `continue` Statements

The `break` and `continue` statements are used to alter the flow of loops in C++. Below are examples and explanations of their use.

---

## 1. The `break` Statement
The `break` statement exits a loop prematurely when a specified condition is met. Once the `break` statement is executed, the program jumps out of the loop and resumes execution at the next statement after the loop.

### Example: Exiting a Loop Early
This program exits the loop when `i` equals 4.

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 0; i < 10; i++) {
        if (i == 4) {
            break; // Exit the loop when i equals 4
        }
        cout << i << "\n";
    }
    return 0;
}
```

### Output:
```
0
1
2
3
```

---

## 2. The `continue` Statement
The `continue` statement skips the current iteration of the loop and proceeds with the next iteration. It is often used when certain conditions need to bypass specific parts of the loop body.

### Example: Skipping an Iteration
This program skips printing the value `4` but continues with the rest of the iterations.

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 0; i < 10; i++) {
        if (i == 4) {
            continue; // Skip this iteration when i equals 4
        }
        cout << i << "\n";
    }
    return 0;
}
```

### Output:
```
0
1
2
3
5
6
7
8
9
```

---

## Key Points
- Use **`break`** to exit a loop completely when a condition is met.
- Use **`continue`** to skip specific iterations of a loop without stopping the entire loop.
- Both statements help improve control over the flow of loops, making programs more efficient and readable.
```