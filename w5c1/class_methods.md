
---

### **Key Concepts**

1. **Methods** are functions that belong to a class and operate on the data members (attributes) of the class.
2. **Two ways to define methods**:
   - **Inside the class definition**: The method is defined directly inside the class block.
   - **Outside the class definition**: The method is declared inside the class and defined later using the **scope resolution operator (::)**.

---

### **Examples**

#### **1. Method Defined Inside the Class**
The method `myMethod` is defined directly in the class.

```cpp
#include <iostream>
using namespace std;

class MyClass {
public:
    void greet() {  // Method defined inside the class
        cout << "Hello from inside the class!\n";
    }
};

int main() {
    MyClass obj;  // Create an object of MyClass
    obj.greet();  // Call the method
    return 0;
}
```

---

#### **2. Method Defined Outside the Class**
The method `greet` is declared inside the class but defined outside using the `::` operator.

```cpp
#include <iostream>
using namespace std;

class MyClass {
public:
    void greet();  // Method declaration
};

// Method definition outside the class
void MyClass::greet() {
    cout << "Hello from outside the class!\n";
}

int main() {
    MyClass obj;  // Create an object of MyClass
    obj.greet();  // Call the method
    return 0;
}
```

---

#### **3. Using Parameters in Methods**
Methods can accept parameters just like regular functions.

```cpp
#include <iostream>
using namespace std;

class Calculator {
public:
    int add(int a, int b) {  // Method with parameters
        return a + b;
    }
};

int main() {
    Calculator calc;
    cout << "Sum: " << calc.add(5, 3) << "\n";  // Output: Sum: 8
    return 0;
}
```

---

#### **4. Returning Values from Methods**
A method can return a value.

```cpp
#include <iostream>
using namespace std;

class Rectangle {
public:
    int area(int length, int width) {
        return length * width;  // Calculate and return the area
    }
};

int main() {
    Rectangle rect;
    cout << "Area: " << rect.area(4, 5) << "\n";  // Output: Area: 20
    return 0;
}
```

---

#### **5. Accessing Class Attributes in Methods**
Methods can use and modify the class’s attributes.

```cpp
#include <iostream>
using namespace std;

class Person {
public:
    string name;

    void setName(string newName) {
        name = newName;  // Assign the value to the attribute
    }

    void introduce() {
        cout << "Hello, my name is " << name << ".\n";
    }
};

int main() {
    Person person;
    person.setName("Alice");  // Set the name using a method
    person.introduce();       // Output: Hello, my name is Alice.
    return 0;
}
```

---

#### **6. Using `this` Keyword**
The `this` pointer refers to the current object. It is useful when you want to distinguish between class attributes and method parameters with the same name.

```cpp
#include <iostream>
using namespace std;

class Person {
private:
    string name;

public:
    void setName(string name) {  // Parameter name conflicts with attribute name
        this->name = name;       // Use 'this' to refer to the class attribute
    }

    string getName() {
        return name;
    }
};

int main() {
    Person person;
    person.setName("Bob");
    cout << "Name: " << person.getName() << "\n";  // Output: Name: Bob
    return 0;
}
```

---

#### **7. Constant Methods**
A constant method ensures that the method cannot modify any class attributes.

```cpp
#include <iostream>
using namespace std;

class Circle {
private:
    double radius;

public:
    Circle(double r) : radius(r) {}

    double getRadius() const {  // Constant method
        return radius;
    }

    void setRadius(double r) {
        radius = r;  // Modify radius (non-const method)
    }
};

int main() {
    Circle c(5.0);
    cout << "Radius: " << c.getRadius() << "\n";  // Output: Radius: 5

    c.setRadius(10.0);
    cout << "New Radius: " << c.getRadius() << "\n";  // Output: New Radius: 10

    return 0;
}
```

---

#### **8. Static Methods**
Static methods belong to the class rather than any specific object. You don’t need an object to call a static method.

```cpp
#include <iostream>
using namespace std;

class Math {
public:
    static int square(int num) {  // Static method
        return num * num;
    }
};

int main() {
    cout << "Square of 4: " << Math::square(4) << "\n";  // Call static method
    return 0;
}
```

---

### **Quick Summary**

| **Concept**           | **Description**                                                                                  | **Example**                     |
|------------------------|--------------------------------------------------------------------------------------------------|----------------------------------|
| **Inside Definition**  | Define the method directly inside the class.                                                    | `void greet() { ... }`          |
| **Outside Definition** | Declare the method in the class and define it later using `::`.                                  | `void MyClass::greet() { ... }` |
| **Parameters**         | Pass values to the method.                                                                       | `void setName(string name)`     |
| **Return Values**      | Methods can return values.                                                                      | `int getValue() { return val; }`|
| **`this` Keyword**     | Refers to the current object, useful for distinguishing between attributes and parameters.        | `this->name = name;`            |
| **Constant Methods**   | Prevent methods from modifying the class’s attributes.                                           | `int getVal() const;`           |
| **Static Methods**     | Methods that don’t depend on a specific object and are called using the class name.              | `Math::square(5)`               |

---

