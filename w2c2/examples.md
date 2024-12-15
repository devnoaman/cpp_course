```markdown
# C++ If...Else Examples

## Example 1: Door Security System
This example demonstrates using `if...else` to simulate a door that opens when the user enters the correct code.

```cpp
#include <iostream>
using namespace std;

int main() {
    int doorCode;
    cout << "Enter the door code: ";
    cin >> doorCode;

    if (doorCode == 1337) {
        cout << "Correct code.\nThe door is now open.\n";
    } else {
        cout << "Wrong code.\nThe door remains closed.\n";
    }

    return 0;
}
```

---

## Example 2: Check Positive, Negative, or Zero
This example shows how to determine whether a number is positive, negative, or zero.

```cpp
#include <iostream>
using namespace std;

int main() {
    int myNum;
    cout << "Enter a number: ";
    cin >> myNum;

    if (myNum > 0) {
        cout << "The value is a positive number.\n";
    } else if (myNum < 0) {
        cout << "The value is a negative number.\n";
    } else {
        cout << "The value is 0.\n";
    }

    return 0;
}
```

---

## Example 3: Voting Eligibility
This example checks if a person is old enough to vote.

```cpp
#include <iostream>
using namespace std;

int main() {
    int age;
    cout << "Enter your age: ";
    cin >> age;

    if (age >= 18) {
        cout << "You are old enough to vote.\n";
    } else {
        cout << "You are not old enough to vote.\n";
    }

    return 0;
}
```

---

## Example 4: Determine Even or Odd
This example demonstrates checking if a number is even or odd.

```cpp
#include <iostream>
using namespace std;

int main() {
    int myNum;
    cout << "Enter a number: ";
    cin >> myNum;

    if (myNum % 2 == 0) {
        cout << myNum << " is even.\n";
    } else {
        cout << myNum << " is odd.\n";
    }

    return 0;
}
```

---

## Key Concepts
1. **`if` Statements**: Used for simple conditions.
2. **`else` Statements**: Executes if the `if` condition is false.
3. **`else if` Statements**: Adds additional conditions when the initial `if` condition is false.
4. **Nested Conditions**: Combine multiple conditions for advanced decision-making.

---
```