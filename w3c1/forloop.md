```markdown
# C++ For Loop

The `for` loop is used when you know the exact number of iterations you want to perform.

---

## Syntax
```cpp
for (statement 1; statement 2; statement 3) {
  // code block to be executed
}
```

- **Statement 1**: Executed once before the loop starts (e.g., initialize a variable).
- **Statement 2**: Defines the condition for the loop to run. If `false`, the loop stops.
- **Statement 3**: Executed after each iteration (e.g., increment/decrement a variable).

---

## Example 1: Counting from 0 to 4
This example demonstrates a simple `for` loop.

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 0; i < 5; i++) {
        cout << i << "\n"; // Print the current value of i
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

### Explanation:
1. **Statement 1**: `int i = 0;` initializes `i` to `0`.
2. **Statement 2**: `i < 5` checks if `i` is less than `5`.
3. **Statement 3**: `i++` increments `i` by `1` after each iteration.

---

## Example 2: Print Even Numbers from 0 to 10
This example demonstrates skipping values by modifying the increment step.

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 0; i <= 10; i = i + 2) {
        cout << i << "\n"; // Print even numbers
    }
    return 0;
}
// Output:
// 0
// 2
// 4
// 6
// 8
// 10
```

### Explanation:
- **Initialization**: `int i = 0;` starts with `i` as 0.
- **Condition**: `i <= 10` ensures the loop runs while `i` is less than or equal to 10.
- **Increment**: `i = i + 2` increases `i` by 2, skipping odd numbers.

---

## Notes
- Use `for` loops for scenarios where the number of iterations is predetermined.
- You can replace **Statement 1**, **Statement 2**, or **Statement 3** with empty statements if they are not required.

Example with omitted statements:
```cpp
int i = 0;
for (; i < 5;) {
  cout << i << "\n";
  i++;
}
```
This behaves the same as the earlier examples but moves initialization and increment outside the `for` loop header.
```