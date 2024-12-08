
```markdown
# C++ Structures (struct)

Structures, or `struct`, allow grouping of related variables under one entity, even if they are of different data types. They are a key feature in C++ for organizing complex data.

---

## What Are Structures?

A **structure** groups variables (members) under one name.  
Unlike arrays, which hold elements of the same type, structures can contain variables of different types.

---

## Declaring and Using Structures

### Basic Structure Declaration
```cpp
struct {
    int myNum;         // Member (int variable)
    string myString;   // Member (string variable)
} myStructure;        // Structure variable
```

### Accessing Members
To access a structure's members, use the **dot operator (`.`)**.

#### Example:
```cpp
struct {
    int myNum;
    string myString;
} myStructure;

int main() {
    // Assign values
    myStructure.myNum = 42;
    myStructure.myString = "Hello World";

    // Access and print
    cout << myStructure.myNum << "\n";
    cout << myStructure.myString << "\n";

    return 0;
}
```

---

## Using One Structure with Multiple Variables

You can create multiple variables from a single structure using commas.

#### Example:
```cpp
struct {
    string brand;
    string model;
    int year;
} car1, car2;

int main() {
    // Assign values to car1
    car1.brand = "BMW";
    car1.model = "X5";
    car1.year = 1999;

    // Assign values to car2
    car2.brand = "Ford";
    car2.model = "Mustang";
    car2.year = 1969;

    // Print values
    cout << car1.brand << " " << car1.model << " " << car1.year << "\n";
    cout << car2.brand << " " << car2.model << " " << car2.year << "\n";

    return 0;
}
```

---

## Named Structures

You can assign a name to a structure to use it as a **data type** throughout your program.

### Syntax:
```cpp
struct StructureName {
    dataType member1;
    dataType member2;
    // Add more members as needed
};
```

### Example: Named Structure
```cpp
struct Car {
    string brand;
    string model;
    int year;
};

int main() {
    // Create variables of type Car
    Car car1, car2;

    // Assign values to car1
    car1.brand = "Tesla";
    car1.model = "Model S";
    car1.year = 2020;

    // Assign values to car2
    car2.brand = "Toyota";
    car2.model = "Corolla";
    car2.year = 2010;

    // Print values
    cout << car1.brand << " " << car1.model << " " << car1.year << "\n";
    cout << car2.brand << " " << car2.model << " " << car2.year << "\n";

    return 0;
}
```

---

## Why Use Structures?

1. **Organized Data**: Combine related variables into a single unit.
2. **Better Code Readability**: Grouping related data improves clarity.
3. **Flexibility**: Members can be of different types, making it easier to represent real-world objects.

---

## Example Use Case: Representing a Person
```cpp
struct Person {
    string name;
    int age;
    double height;
};

int main() {
    // Create and initialize
    Person person1;
    person1.name = "Alice";
    person1.age = 30;
    person1.height = 5.6;

    // Output details
    cout << "Name: " << person1.name << "\n";
    cout << "Age: " << person1.age << "\n";
    cout << "Height: " << person1.height << " ft\n";

    return 0;
}
```

---

## Advanced Usage: Arrays of Structures

Structures can be combined with arrays to store multiple objects of the same type.

#### Example:
```cpp
struct Car {
    string brand;
    string model;
    int year;
};

int main() {
    // Array of structures
    Car cars[2];

    // Assign values
    cars[0] = {"BMW", "X5", 1999};
    cars[1] = {"Audi", "A4", 2021};

    // Print details
    for (int i = 0; i < 2; i++) {
        cout << cars[i].brand << " " << cars[i].model << " " << cars[i].year << "\n";
    }

    return 0;
}
```

---

## Structures vs. Classes

While structures and classes are similar in C++:
- **Structure** members are public by default.
- **Class** members are private by default.

#### Example:
```cpp
struct MyStruct {
    int num;  // Public by default
};

class MyClass {
    int num;  // Private by default
};
```

---

## Summary

- Structures are a way to group related variables.
- They support different data types within a single unit.
- Named structures allow reusability as custom data types.
- Structures can be combined with arrays for advanced data storage.

Mastering structures will help you organize and manage complex data in C++ programs!
```