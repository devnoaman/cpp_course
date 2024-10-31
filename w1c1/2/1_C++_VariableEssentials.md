
---

# C++ Variable Essentials

## Module 1: Introduction to C++ Variables

### What Are Variables?
Variables in C++ act as containers to store various types of data. Each variable type allows for storing different kinds of information, from whole numbers to text.

- **int** - Stores integers, such as 123 or -123
- **double** - Stores floating-point numbers with decimals, such as 19.99
- **char** - Stores a single character, such as 'a' or 'B'
- **string** - Stores text, like "Hello World"
- **bool** - Stores two states: `true` or `false`

> **Activity**: Identify real-world scenarios for each type of variable (e.g., `int` for counting items, `double` for price).

---

## Module 2: Declaring Variables

### Basics of Variable Declaration

To declare a variable in C++, specify the type and give it a name:

```cpp
type variableName = value;
```

- **type** - The data type (e.g., `int`, `double`).
- **variableName** - Your chosen name for the variable.

Example:  
Declare a variable `myNum` of type `int` with a value of 15.

```cpp
int myNum = 15;
cout << myNum;  // Outputs: 15
```

> **Activity**: Create your own variables for common items like age, temperature, or first name.

---

## Module 3: Working with Variable Assignment

### Assigning and Reassigning Values

Variables can be assigned initial values or updated with new values. Changing a variable's value will overwrite the previous data.

Example:

```cpp
int myNum = 15;   // myNum is 15
myNum = 10;       // Now myNum is 10
cout << myNum;    // Outputs: 10
```

> **Practice**: Experiment with changing values in various variables to understand how reassignment works.

---

## Module 4: Types of Variables and Their Applications

### Common Types and Their Uses

1. **Integer (`int`)**: Count objects or people.
2. **Double (`double`)**: Work with prices, averages, or measurements.
3. **Character (`char`)**: Store a single letter or symbol.
4. **String (`string`)**: Capture text like names, messages.
5. **Boolean (`bool`)**: Represent binary states (on/off, yes/no).

> **Project**: Build a simple profile page using these variable types to store a person's name, age, and favorite character.

---

## Module 5: Dynamic Variables and Scope

### Declaring Without Assignment

Variables can be declared without assigning an initial value and updated later:

```cpp
int score;
score = 50;
cout << score;  // Outputs: 50
```

> **Challenge**: Think of three situations where you might not know a value initially and update it later (e.g., score in a game, timer value).

---

## Module 6: Final Project

### Application: Personal Information Organizer

Create a mini C++ program that uses different types of variables to store and display a person’s basic details (name, age, favorite number, and so on). Use `cout` to output a formatted summary of this information.

