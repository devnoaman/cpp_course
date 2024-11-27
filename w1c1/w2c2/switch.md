```markdown
# C++ Switch Statements

The `switch` statement is used to select one of many code blocks to be executed based on the value of an expression.

---

## Syntax

```cpp
switch (expression) {
  case x:
    // Code block
    break;
  case y:
    // Code block
    break;
  default:
    // Code block
}
```

### How It Works
1. The `switch` expression is evaluated once.
2. The value of the expression is compared with each `case`.
3. If a match is found, the associated code block is executed.
4. The `break` statement stops further case testing and exits the switch.
5. The `default` block (optional) executes if no `case` matches.

---

## Example: Weekday Names

The example below maps a numeric day (1–7) to the corresponding weekday name:

```cpp
#include <iostream>
using namespace std;

int main() {
    int day = 4;

    switch (day) {
        case 1:
            cout << "Monday";
            break;
        case 2:
            cout << "Tuesday";
            break;
        case 3:
            cout << "Wednesday";
            break;
        case 4:
            cout << "Thursday";
            break;
        case 5:
            cout << "Friday";
            break;
        case 6:
            cout << "Saturday";
            break;
        case 7:
            cout << "Sunday";
            break;
        default:
            cout << "Invalid day";
    }

    return 0;
}
// Outputs: "Thursday" (day 4)
```

---

## The `break` Keyword
The `break` keyword is essential to terminate a `case`. Without it, the program will continue executing subsequent cases (fall-through behavior).

Example without `break`:
```cpp
int day = 2;
switch (day) {
    case 1:
        cout << "Monday";
    case 2:
        cout << "Tuesday";
    case 3:
        cout << "Wednesday";
}
// Outputs: "TuesdayWednesday"
```

---

## The `default` Keyword
The `default` keyword specifies code to execute if no cases match.

```cpp
#include <iostream>
using namespace std;

int main() {
    int day = 8;

    switch (day) {
        case 6:
            cout << "Today is Saturday";
            break;
        case 7:
            cout << "Today is Sunday";
            break;
        default:
            cout << "Looking forward to the Weekend";
    }

    return 0;
}
// Outputs: "Looking forward to the Weekend"
```

---

## Key Points
1. **Switch Expression**: Must evaluate to an integer or character (not a floating-point or string).
2. **Break Statement**: Prevents fall-through to subsequent cases.
3. **Default Statement**: Handles unmatched cases; optional but useful.
4. **Efficiency**: Ideal for decision trees with many options.

---
```