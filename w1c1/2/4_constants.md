
---

# C++ Constants

## Module 1: What Are Constants?

In C++, a **constant** is a variable whose value cannot be changed once it’s set. By declaring a variable as constant, you ensure its value remains **unchangeable** and **read-only**. This is useful for values that are unlikely to change, such as mathematical constants or fixed settings.

To declare a constant variable, use the `const` keyword.

#### Example

```cpp
const int myNum = 15;  // myNum is permanently set to 15
myNum = 10;            // Error: assignment of read-only variable 'myNum'
```

---

## Module 2: When to Use Constants

Use constants for values that:
- Are fixed and should not change during the program’s execution.
- Help improve readability by giving meaningful names to hardcoded values.

#### Examples

```cpp
const int minutesPerHour = 60;
const float PI = 3.14;
```

> **Tip**: Constants make code more readable by providing clear labels for fixed values.

---

## Module 3: Declaring Constants

### Key Points

1. **Immediate Assignment**: A constant must be assigned a value when it’s declared.
   - **Correct**: `const int minutesPerHour = 60;`
   - **Incorrect**: `const int minutesPerHour;` (error: unassigned constant)

2. **Read-Only Behavior**: Once assigned, attempting to modify a constant will result in a compilation error.

#### Example of an Error

```cpp
const int daysInWeek = 7;
daysInWeek = 8;  // Error: assignment of read-only variable 'daysInWeek'
```

---

## Module 4: Best Practices and Usage

1. **Naming Conventions**: Use descriptive names for constants, often in uppercase, to distinguish them from variables (e.g., `MAX_USERS`, `PI`).
2. **Usage**: Commonly used for fixed values in calculations, settings, and application limits.

---

## Module 5: Practice Exercise

### Using Constants in a Program

1. Define constants for key settings, such as:
   - `const int MAX_USERS = 100;`
   - `const float TAX_RATE = 0.07;`

2. Write a small program that uses these constants to calculate values (e.g., total tax or user limits) and observe how constants help improve readability and prevent accidental changes.

Constants are a simple way to safeguard your code from unintended modifications and make it more understandable!