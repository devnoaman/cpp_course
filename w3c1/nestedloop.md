```markdown
# C++ Nested Loops

Nested loops are loops placed inside other loops. The **inner loop** runs completely for each iteration of the **outer loop**.

---

## Example: Nested `for` Loops
The following example demonstrates a nested loop, where the **outer loop** controls the rows and the **inner loop** controls the columns.

```cpp
#include <iostream>
using namespace std;

int main() {
    // Outer loop
    for (int i = 1; i <= 2; ++i) {
        cout << "Outer: " << i << "\n"; // Executes 2 times

        // Inner loop
        for (int j = 1; j <= 3; ++j) {
            cout << " Inner: " << j << "\n"; // Executes 6 times (2 * 3)
        }
    }
    return 0;
}
```

### Output:
```
Outer: 1
 Inner: 1
 Inner: 2
 Inner: 3
Outer: 2
 Inner: 1
 Inner: 2
 Inner: 3
```

---

## Example: Generating a Multiplication Table
Nested loops are useful for creating tables, grids, or similar structures.

```cpp
#include <iostream>
using namespace std;

int main() {
    // Rows of the table
    for (int i = 1; i <= 5; ++i) {
        // Columns of the table
        for (int j = 1; j <= 5; ++j) {
            cout << i * j << "\t"; // Print product with tab space
        }
        cout << "\n"; // New line after each row
    }
    return 0;
}
```

### Output:
```
1   2   3   4   5
2   4   6   8   10
3   6   9   12  15
4   8   12  16  20
5   10  15  20  25
```

---

## Key Points
1. **Execution Order**:
   - The **outer loop** runs first, and for each iteration of the outer loop, the **inner loop** runs completely.
2. **Performance**:
   - Nested loops can be computationally expensive as the total iterations are the product of the iterations of the inner and outer loops.
3. **Practical Applications**:
   - Generating tables, patterns, grids, or working with 2D arrays/matrices.

---

## Example: Creating a Star Pattern
This example demonstrates creating a triangle pattern using nested loops.

```cpp
#include <iostream>
using namespace std;

int main() {
    int rows = 5;

    for (int i = 1; i <= rows; ++i) {
        for (int j = 1; j <= i; ++j) {
            cout << "* ";
        }
        cout << "\n";
    }
    return 0;
}
```

### Output:
```
* 
* * 
* * * 
* * * * 
* * * * * 
```
```