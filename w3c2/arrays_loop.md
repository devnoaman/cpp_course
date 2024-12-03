```markdown
# C++ Arrays and Loops

Arrays can be traversed using loops to perform operations on their elements. Both traditional `for` loops and modern **for-each loops** (introduced in C++11) are widely used.

---

## Looping Through an Array with a `for` Loop
A traditional `for` loop is commonly used to iterate through arrays. It provides access to both the element and its index.

---

### Example 1: Basic Traversal
```cpp
#include <iostream>
using namespace std;

int main() {
    string cars[5] = {"Volvo", "BMW", "Ford", "Mazda", "Tesla"};

    // Loop through the array elements
    for (int i = 0; i < 5; i++) {
        cout << cars[i] << "\n";
    }

    return 0;
}
```

### Output:
```
Volvo
BMW
Ford
Mazda
Tesla
```

---

### Example 2: Accessing Indices and Values
```cpp
#include <iostream>
using namespace std;

int main() {
    string cars[5] = {"Volvo", "BMW", "Ford", "Mazda", "Tesla"};

    // Loop through and print index and value
    for (int i = 0; i < 5; i++) {
        cout << i << " = " << cars[i] << "\n";
    }

    return 0;
}
```

### Output:
```
0 = Volvo
1 = BMW
2 = Ford
3 = Mazda
4 = Tesla
```

---

### Example 3: Looping Through an Array of Integers
```cpp
#include <iostream>
using namespace std;

int main() {
    int myNumbers[5] = {10, 20, 30, 40, 50};

    // Loop through integer array
    for (int i = 0; i < 5; i++) {
        cout << myNumbers[i] << "\n";
    }

    return 0;
}
```

### Output:
```
10
20
30
40
50
```

---

## Using a **For-Each Loop** (C++11)
The **for-each loop** simplifies iteration by eliminating the need for manual indexing. It's particularly useful for read-only operations on arrays.

---

### Syntax:
```cpp
for (type variableName : arrayName) {
    // code block to execute
}
```

---

### Example 4: Loop Through Integers
```cpp
#include <iostream>
using namespace std;

int main() {
    int myNumbers[5] = {10, 20, 30, 40, 50};

    // For-each loop to traverse the array
    for (int i : myNumbers) {
        cout << i << "\n";
    }

    return 0;
}
```

### Output:
```
10
20
30
40
50
```

---

### Example 5: Loop Through Strings
```cpp
#include <iostream>
using namespace std;

int main() {
    string cars[5] = {"Volvo", "BMW", "Ford", "Mazda", "Tesla"};

    // For-each loop for strings
    for (string car : cars) {
        cout << car << "\n";
    }

    return 0;
}
```

### Output:
```
Volvo
BMW
Ford
Mazda
Tesla
```

---

## Key Points:
1. Use traditional `for` loops when:
   - You need the index of elements.
   - You're modifying elements.
2. Use for-each loops when:
   - You only need to read the elements.
   - Simplicity is preferred.
```