```markdown
# C++ Arrays

An array in C++ is a collection of elements of the same type stored in contiguous memory locations. Arrays allow you to store multiple values in a single variable.

---

## Declaring an Array
To declare an array, specify:
1. The data type.
2. The array name.
3. The number of elements in square brackets `[]`.

### Syntax:
```cpp
type arrayName[arraySize];
```

### Example:
```cpp
string cars[4]; // An array of 4 strings
```

---

## Initializing an Array
You can initialize an array with values using an array literal. Values are specified in curly braces `{}`, separated by commas.

### Examples:
```cpp
string cars[4] = {"Volvo", "BMW", "Ford", "Mazda"};
int myNum[3] = {10, 20, 30};
```

---

## Accessing Array Elements
You can access elements in an array using their **index**. Note that array indices in C++ start from `0`.

### Example:
```cpp
#include <iostream>
using namespace std;

int main() {
    string cars[4] = {"Volvo", "BMW", "Ford", "Mazda"};
    cout << cars[0]; // Outputs "Volvo"
    return 0;
}
```

### Output:
```
Volvo
```

---

## Modifying Array Elements
You can change an element by assigning a new value to its index.

### Example:
```cpp
#include <iostream>
using namespace std;

int main() {
    string cars[4] = {"Volvo", "BMW", "Ford", "Mazda"};
    cars[0] = "Tesla"; // Modify the first element
    cout << cars[0];    // Outputs "Tesla"
    return 0;
}
```

### Output:
```
Tesla
```

---

## Looping Through an Array
You can use loops to iterate through the elements of an array.

### Example: Using a `for` loop
```cpp
#include <iostream>
using namespace std;

int main() {
    string cars[4] = {"Volvo", "BMW", "Ford", "Mazda"};
    for (int i = 0; i < 4; i++) {
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
```

---

## Key Points
- Arrays are fixed in size; the size must be specified at compile time.
- Array indices start from `0` and go up to `arraySize - 1`.
- Use loops to efficiently access and modify array elements.
```