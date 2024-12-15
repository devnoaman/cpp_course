

---

### **What is a Constructor?**

- A **constructor** is a special method in a class that is **automatically called** when an object is created.
- The **constructor name** is the **same as the class name**.
- **Characteristics of a Constructor**:
  - Does not have a return type (not even `void`).
  - Typically used to initialize the attributes of an object.
  - Can have parameters (to set specific values during object creation).
  - Can be defined inside or outside the class using the **scope resolution operator (`::`)**.

---

### **Types of Constructors**

1. **Default Constructor**  
   - A constructor with no parameters.
2. **Parameterized Constructor**  
   - A constructor that accepts parameters to initialize attributes.
3. **Copy Constructor**  
   - A special constructor used to create a copy of an object.

---

### **1. Default Constructor**
A constructor with no arguments is called automatically when an object is created.

```cpp
#include <iostream>
using namespace std;

class MyClass {
public:
    MyClass() {  // Default constructor
        cout << "Default Constructor Called\n";
    }
};

int main() {
    MyClass obj;  // Calls the default constructor
    return 0;
}
```

---

### **2. Parameterized Constructor**
Constructors can take arguments to initialize attributes directly.

```cpp
#include <iostream>
using namespace std;

class Car {
public:
    string brand;
    string model;
    int year;

    // Parameterized constructor
    Car(string b, string m, int y) {
        brand = b;
        model = m;
        year = y;
    }
};

int main() {
    Car car1("Toyota", "Corolla", 2020);  // Initialize with values
    Car car2("Honda", "Civic", 2018);

    cout << car1.brand << " " << car1.model << " " << car1.year << "\n";
    cout << car2.brand << " " << car2.model << " " << car2.year << "\n";
    return 0;
}
```

---

### **3. Constructor Defined Outside the Class**
A constructor can be declared in the class and defined later outside it.

```cpp
#include <iostream>
using namespace std;

class Car {
public:
    string brand;
    string model;
    int year;

    Car(string b, string m, int y);  // Declaration
};

// Definition outside the class
Car::Car(string b, string m, int y) {
    brand = b;
    model = m;
    year = y;
}

int main() {
    Car car1("Ford", "Mustang", 1967);
    Car car2("Chevrolet", "Camaro", 1969);

    cout << car1.brand << " " << car1.model << " " << car1.year << "\n";
    cout << car2.brand << " " << car2.model << " " << car2.year << "\n";
    return 0;
}
```

---

### **4. Copy Constructor**
A **copy constructor** initializes an object by copying attributes from another object of the same class.

```cpp
#include <iostream>
using namespace std;

class MyClass {
public:
    int value;

    // Parameterized constructor
    MyClass(int val) {
        value = val;
    }

    // Copy constructor
    MyClass(const MyClass &obj) {
        value = obj.value;  // Copy value
    }
};

int main() {
    MyClass obj1(42);        // Initialize with parameterized constructor
    MyClass obj2 = obj1;     // Calls the copy constructor

    cout << "obj1 value: " << obj1.value << "\n";
    cout << "obj2 value: " << obj2.value << "\n";
    return 0;
}
```

---

### **5. Constructor Overloading**
You can define multiple constructors in a class with different sets of parameters. This is known as **constructor overloading**.

```cpp
#include <iostream>
using namespace std;

class Box {
public:
    double length, width, height;

    // Default constructor
    Box() {
        length = width = height = 1.0;  // Default dimensions
    }

    // Parameterized constructor
    Box(double l, double w, double h) {
        length = l;
        width = w;
        height = h;
    }

    void display() {
        cout << "Dimensions: " << length << " x " << width << " x " << height << "\n";
    }
};

int main() {
    Box defaultBox;             // Calls default constructor
    Box customBox(5.0, 3.0, 2.0);  // Calls parameterized constructor

    defaultBox.display();  // Output: Dimensions: 1 x 1 x 1
    customBox.display();   // Output: Dimensions: 5 x 3 x 2

    return 0;
}
```

---

### **6. Explicit Constructor**
Using the `explicit` keyword prevents implicit conversions when using a single-argument constructor.

```cpp
#include <iostream>
using namespace std;

class Test {
public:
    int value;

    explicit Test(int val) {  // Explicit constructor
        value = val;
    }
};

int main() {
    Test obj(5);  // Explicitly calls the constructor

    // Test obj2 = 10;  // Error: Cannot implicitly convert int to Test
    cout << "Value: " << obj.value << "\n";
    return 0;
}
```

---

### **7. Using Initializer Lists in Constructors**
Instead of assigning values inside the constructor body, you can use an **initializer list** for better performance.

```cpp
#include <iostream>
using namespace std;

class Rectangle {
private:
    int length, width;

public:
    // Constructor with initializer list
    Rectangle(int l, int w) : length(l), width(w) {}

    void display() {
        cout << "Length: " << length << ", Width: " << width << "\n";
    }
};

int main() {
    Rectangle rect(10, 5);
    rect.display();  // Output: Length: 10, Width: 5
    return 0;
}
```

---

### **Quick Summary**

| **Feature**               | **Description**                                                               | **Example**                                |
|----------------------------|-------------------------------------------------------------------------------|-------------------------------------------|
| **Default Constructor**    | No parameters, initializes attributes with default values.                   | `MyClass() { ... }`                       |
| **Parameterized Constructor** | Accepts parameters to initialize attributes.                                 | `Car(string b, int y) { ... }`            |
| **Copy Constructor**       | Creates a new object as a copy of an existing object.                        | `MyClass(const MyClass &obj) { ... }`     |
| **Overloaded Constructor** | Multiple constructors with different sets of parameters.                     | `Box()`, `Box(double l, double w)`        |
| **Explicit Constructor**   | Prevents implicit conversions.                                               | `explicit MyClass(int x) { ... }`         |
| **Initializer List**       | Initializes attributes directly in the constructor's initializer list.       | `Rectangle(int l, int w) : length(l) { }` |

---

