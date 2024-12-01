```markdown
# C++ `for` Loop Examples

`for` loops are used for iterating over a block of code a known number of times. Below are practical examples demonstrating various real-life uses of `for` loops.

---

## 1. Counting by Tens
This program counts from 0 to 100 in increments of 10.

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 0; i <= 100; i += 10) {
        cout << i << "\n";
    }
    return 0;
}
```

### Output:
```
0
10
20
30
40
50
60
70
80
90
100
```

---

## 2. Printing Even Numbers
This program prints even numbers between 0 and 10 (inclusive).

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 0; i <= 10; i += 2) {
        cout << i << "\n";
    }
    return 0;
}
```

### Output:
```
0
2
4
6
8
10
```

---

## 3. Printing Odd Numbers
This program prints odd numbers between 1 and 10.

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 10; i += 2) {
        cout << i << "\n";
    }
    return 0;
}
```

### Output:
```
1
3
5
7
9
```

---

## 4. Powers of 2
This program prints the powers of 2 up to 512.

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 2; i <= 512; i *= 2) {
        cout << i << "\n";
    }
    return 0;
}
```

### Output:
```
2
4
8
16
32
64
128
256
512
```

---

## 5. Multiplication Table
This program prints the multiplication table for a specified number (e.g., 2).

```cpp
#include <iostream>
using namespace std;

int main() {
    int number = 2;

    for (int i = 1; i <= 10; i++) {
        cout << number << " x " << i << " = " << number * i << "\n";
    }
    return 0;
}
```

### Output:
```
2 x 1 = 2
2 x 2 = 4
2 x 3 = 6
2 x 4 = 8
2 x 5 = 10
2 x 6 = 12
2 x 7 = 14
2 x 8 = 16
2 x 9 = 18
2 x 10 = 20
```

---

## Key Points
- The `for` loop simplifies iterating over a range of values with a known number of iterations.
- It is commonly used in mathematical operations, tables, and controlled iterations.
```