```markdown
# C++ Operators

Operators in C++ allow us to perform operations on variables and values. Each operator has a specific purpose, whether it's arithmetic, assignment, comparison, logical, or bitwise. Let's go through each type of operator with examples.

---

## 1. Arithmetic Operators

Arithmetic operators are used for basic mathematical calculations, like addition, subtraction, and multiplication.

| Operator | Name          | Description                          | Example       |
|----------|---------------|--------------------------------------|---------------|
| `+`      | Addition      | Adds two values                      | `x + y`       |
| `-`      | Subtraction   | Subtracts one value from another     | `x - y`       |
| `*`      | Multiplication| Multiplies two values                | `x * y`       |
| `/`      | Division      | Divides one value by another         | `x / y`       |
| `%`      | Modulus       | Returns the division remainder       | `x % y`       |
| `++`     | Increment     | Increases the value of a variable by 1 | `++x`       |
| `--`     | Decrement     | Decreases the value of a variable by 1 | `--x`       |

### Example

```cpp
int a = 10, b = 3;
cout << "Addition: " << a + b << endl;      // 13
cout << "Subtraction: " << a - b << endl;   // 7
cout << "Multiplication: " << a * b << endl; // 30
cout << "Division: " << a / b << endl;      // 3
cout << "Modulus: " << a % b << endl;       // 1
a++;                                        // Increment a to 11
b--;                                        // Decrement b to 2
```

---

## 2. Assignment Operators

Assignment operators assign values to variables. The `=` operator is the simplest, but there are others for performing operations and assigning values in a single step.

| Operator | Name              | Example   | Equivalent to     |
|----------|-------------------|-----------|-------------------|
| `=`      | Assignment        | `x = 5`   | `x = 5`          |
| `+=`     | Addition Assignment | `x += 3` | `x = x + 3`      |
| `-=`     | Subtraction Assignment | `x -= 3` | `x = x - 3`   |
| `*=`     | Multiplication Assignment | `x *= 3` | `x = x * 3` |
| `/=`     | Division Assignment | `x /= 3` | `x = x / 3`    |
| `%=`     | Modulus Assignment | `x %= 3` | `x = x % 3`    |

### Example

```cpp
int x = 5;
x += 2;  // Now x is 7
x -= 1;  // Now x is 6
x *= 3;  // Now x is 18
x /= 2;  // Now x is 9
x %= 4;  // Now x is 1
```

---

## 3. Comparison Operators

Comparison operators compare two values and return `true` or `false` based on the result. They are commonly used in conditional statements.

| Operator | Name             | Description                              | Example       |
|----------|------------------|------------------------------------------|---------------|
| `==`     | Equal to         | Checks if two values are equal           | `x == y`      |
| `!=`     | Not equal to     | Checks if two values are not equal       | `x != y`      |
| `<`      | Less than        | Checks if the left value is smaller      | `x < y`       |
| `>`      | Greater than     | Checks if the left value is larger       | `x > y`       |
| `<=`     | Less than or equal to | Checks if the left value is smaller or equal | `x <= y` |
| `>=`     | Greater than or equal to | Checks if the left value is larger or equal | `x >= y` |

### Example

```cpp
int age = 20;
if (age >= 18) {
    cout << "Eligible to vote." << endl;
} else {
    cout << "Not eligible to vote." << endl;
}
```

---

## 4. Logical Operators

Logical operators are used to combine multiple conditions. They return `true` or `false` based on the logical relationship between the conditions.

| Operator | Name  | Description                                        | Example                |
|----------|-------|----------------------------------------------------|------------------------|
| `&&`     | AND   | Returns `true` if both conditions are true         | `(x > 5 && x < 10)`   |
| `||`     | OR    | Returns `true` if at least one condition is true   | `(x > 5 || x < 3)`    |
| `!`      | NOT   | Reverses the logical state of its operand          | `!(x > 5)`            |

### Example

```cpp
int score = 85;
if (score >= 80 && score <= 100) {
    cout << "Great job!" << endl;
} else if (score >= 50 || score < 80) {
    cout << "Good effort!" << endl;
} else {
    cout << "Needs improvement." << endl;
}
```

---

## 5. Bitwise Operators

Bitwise operators work at the binary level, manipulating the bits of an integer. These are more advanced but useful for low-level programming.

| Operator | Name         | Description                           | Example       |
|----------|--------------|---------------------------------------|---------------|
| `&`      | AND          | Performs a binary AND operation      | `x & y`       |
| `|`      | OR           | Performs a binary OR operation       | `x | y`       |
| `^`      | XOR          | Performs a binary XOR operation      | `x ^ y`       |
| `~`      | NOT          | Performs a binary NOT operation      | `~x`          |
| `<<`     | Left Shift   | Shifts bits to the left              | `x << 1`      |
| `>>`     | Right Shift  | Shifts bits to the right             | `x >> 1`      |

### Example

```cpp
int x = 5;  // Binary: 0101
int y = 3;  // Binary: 0011
cout << (x & y) << endl;  // Outputs 1 (Binary: 0001)
cout << (x | y) << endl;  // Outputs 7 (Binary: 0111)
cout << (x ^ y) << endl;  // Outputs 6 (Binary: 0110)
cout << (~x) << endl;     // Outputs -6 (Binary: 1010)
```

---

## Summary

Operators are essential in C++ for performing calculations, making comparisons, and controlling the flow of logic in a program. Understanding these operators is key to building functional and efficient C++ code.

--- 

### Practice Exercise

Write a program that takes two numbers as input and:

1. Outputs their sum, difference, product, and quotient.
2. Checks if the first number is greater than, less than, or equal to the second number.
3. Uses logical operators to check if both numbers are positive or if at least one of them is negative.
```