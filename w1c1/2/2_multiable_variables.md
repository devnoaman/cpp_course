
---

# C++ Declaring Multiple Variables

## Module 1: Declaring Multiple Variables

### Declaring Several Variables of the Same Type

In C++, you can declare multiple variables of the same type in a single line, separated by commas. This can help make your code more concise and easier to read.

#### Example

```cpp
int x = 5, y = 6, z = 50;
cout << x + y + z;  // Outputs: 61
```

In this example:
- `x`, `y`, and `z` are all declared as `int`.
- They are assigned values of `5`, `6`, and `50`, respectively.

> **Activity**: Try declaring three more integer variables and assign them different values in a single line. Use `cout` to print the sum of these variables.

---

## Module 2: Assigning the Same Value to Multiple Variables

You can assign the same value to multiple variables in one line by chaining the assignment operator (`=`). This is especially useful when you want to initialize several variables to the same starting value.

#### Example

```cpp
int x, y, z;
x = y = z = 50;
cout << x + y + z;  // Outputs: 150
```

In this example:
- `x`, `y`, and `z` are all assigned the value `50`.
- Each variable will have the same value, which can be useful for initializing counters, settings, or default values.

> **Activity**: Use the technique above to assign the value `100` to three new variables (`a`, `b`, and `c`). Output their total value.

---

## Module 3: Practical Application and Exercises

### Grouping and Reassigning Variables

1. **Declare & Assign**: Declare three floating-point variables (`float`) in a single line, assigning different values to each. Output the average of these variables.
  
2. **Assign the Same Value**: Declare three string variables (`string name1, name2, name3`) and set them all to "unknown". Change each variable's value individually to represent different names and print them.

---

## Module 4: Final Project

### Team Score Tracker

Create a simple score-tracking program:
- Declare three integer variables `score1`, `score2`, and `score3`.
- Set each score to an initial value of `0` using a single assignment.
- Update each score with new values (e.g., by adding points), and output the total combined score.

This exercise reinforces the concepts of multiple declaration, assignment, and variable updating!