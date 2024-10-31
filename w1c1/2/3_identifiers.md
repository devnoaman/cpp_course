
---

# C++ Identifiers

## Module 1: What Are Identifiers?

In C++, **identifiers** are unique names used to label variables, functions, classes, and other user-defined items. They play a vital role in making code easy to read and understand.

Identifiers can be:
- Short names like `x` or `y`.
- Descriptive names like `age`, `totalVolume`, or `sum`.

> **Best Practice**: Use descriptive names to make your code readable and maintainable.

#### Example

```cpp
// Good
int minutesPerHour = 60;

// OK, but less clear
int m = 60;
```

---

## Module 2: Rules for Naming Identifiers

To create valid identifiers, C++ has some naming rules:

1. **Allowed Characters**: Letters, digits, and underscores (`_`).
2. **Start Character**: Must begin with a letter or underscore.
3. **Case-Sensitive**: `myVar` and `myvar` are different.
4. **No Spaces or Special Characters**: Avoid characters like `!`, `#`, `%`, etc.
5. **Reserved Words**: Keywords like `int` or `return` cannot be used as identifiers.

---

## Module 3: Examples and Best Practices

### Descriptive vs. Non-Descriptive Names

When naming variables, consider the purpose they serve:

- **Descriptive**: `totalCost`, `userAge`, `accountBalance`
- **Non-Descriptive**: `a`, `b`, `c` (only use if the variable’s purpose is clear in context)

#### Example

```cpp
int totalCost = 150;
int a = 150;   // Less clear
```

### Case Sensitivity

Since identifiers are case-sensitive, `MyVar` and `myvar` are different:

```cpp
int myVar = 10;
int myvar = 20;
cout << myVar;   // Outputs 10
cout << myvar;   // Outputs 20
```

---

## Module 4: Practice and Application

### Naming Challenge

1. **Identify**: Which of these are valid identifiers?
   - `userScore`
   - `1stPlace` (Invalid)
   - `total$Amount` (Invalid)

2. **Create Variables**: Write a set of descriptive variables for a user profile (e.g., `userName`, `userAge`, `userScore`).

> **Project**: Create a small C++ program that includes descriptive identifiers for a shopping cart, using variables like `itemPrice`, `quantity`, and `totalCost`.

Following these rules will help you create readable and well-organized code!