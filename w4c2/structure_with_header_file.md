

---

### ** `Calculator.cpp`**
```cpp
// Calculator.cpp
#include "Calculator.h"
#include <iostream>

double Calculator::add() {
    return num1 + num2;
}

double Calculator::subtract() {
    return num1 - num2;
}

double Calculator::multiply() {
    return num1 * num2;
}

double Calculator::divide() {
    if (num2 == 0) {
        std::cout << "Error: Division by zero is not allowed." << std::endl;
        return 0; // Return 0 as an error value
    }
    return num1 / num2;
}
```

---

### ** `main.cpp`**
The main program remains the same, as it does not depend on exceptions anymore:

```cpp
// main.cpp
#include <iostream>
#include "Calculator.h"

using namespace std;

int main() {
    Calculator calc;
    char operation;

    cout << "Enter first number: ";
    cin >> calc.num1;

    cout << "Enter second number: ";
    cin >> calc.num2;

    cout << "Enter operation (+, -, *, /): ";
    cin >> operation;

    switch (operation) {
        case '+':
            cout << "Result: " << calc.add() << endl;
            break;
        case '-':
            cout << "Result: " << calc.subtract() << endl;
            break;
        case '*':
            cout << "Result: " << calc.multiply() << endl;
            break;
        case '/':
            cout << "Result: " << calc.divide() << endl;
            break;
        default:
            cout << "Invalid operation!" << endl;
    }

    return 0;
}
```

---


1. **Division Error Handling**:
   - he `divide` function checks if `num2` is `0` and outputs an error message using `std::cout`.
   - If division by zero occurs, the function returns `0` as an error value.

2. **Simpler Error Reporting**:
   - The `cout` message is sufficient to alert the user about the issue without breaking the flow of the program.

---

### **Output Example**

#### Input:
```
Enter first number: 10
Enter second number: 0
Enter operation (+, -, *, /): /
```

#### Output:
```
Error: Division by zero is not allowed.
Result: 0
```

---


```
use with it while true


  if (operation == 'q' || operation == 'Q') {
            cout << "Goodbye!" << endl;
            break;
        }
```