`#ifndef` is a **preprocessor directive** in C++ (and C) that stands for **"if not defined"**. It is used in conjunction with `#define` and `#endif` to implement **header guards**, which prevent multiple inclusions of the same header file in a program.

---

### **Why Use Header Guards?**

When a header file is included multiple times (directly or indirectly), the compiler will process it multiple times, potentially causing **redefinition errors**. Header guards ensure that a header file's contents are included only once per compilation unit.

---

### **How It Works**

Here's an example:

#### **`MyHeader.h`**
```cpp
#ifndef MYHEADER_H     // Check if MYHEADER_H is not defined
#define MYHEADER_H     // Define MYHEADER_H

// Contents of the header file
struct MyStruct {
    int a;
    double b;
};

#endif // End of the header guard
```

#### **Explanation:**
1. **First Inclusion**:
   - When the header file is included for the first time, `MYHEADER_H` is not defined.
   - The compiler includes the contents of the file and defines `MYHEADER_H`.

2. **Subsequent Inclusions**:
   - If the same file is included again, `MYHEADER_H` is already defined.
   - The `#ifndef` condition evaluates to false, so the file's contents are skipped.

---

### **Usage in Code**

#### **Example with Header Guards**
Suppose you have the following files:

**`header.h`**
```cpp
#ifndef HEADER_H
#define HEADER_H

int add(int a, int b) {
    return a + b;
}

#endif
```

**`main.cpp`**
```cpp
#include "header.h"
#include "header.h" // Included twice

#include <iostream>
using namespace std;

int main() {
    cout << "Sum: " << add(5, 3) << endl;
    return 0;
}
```

When you compile this, **header guards** ensure `header.h` is only processed once, avoiding redefinition errors.

---

### **What Happens Without Header Guards?**

Without header guards, including the same file multiple times can lead to errors like:
```cpp
error: redefinition of ‘int add(int, int)’
```

---

### **Alternative to Header Guards: `#pragma once`**

Modern compilers also support `#pragma once`, which is simpler and ensures the file is included only once:

```cpp
#pragma once

int add(int a, int b) {
    return a + b;
}
```

While `#pragma once` is easier to use, it's not part of the official C++ standard, but it is widely supported.

Let me know if you'd like more clarity!