### **C++ Inheritance**

Inheritance allows a class (called the **derived class** or **child class**) to inherit attributes and methods from another class (called the **base class** or **parent class**). This promotes code reuse and establishes a hierarchical relationship between classes.

---

### **Syntax for Inheritance**

To define inheritance, use the `:` symbol, followed by the **access specifier** (`public`, `protected`, or `private`) and the name of the base class:

```cpp
class DerivedClass : public BaseClass {
    // Additional members of DerivedClass
};
```

---

### **Types of Inheritance in C++**
1. **Single Inheritance**: A class inherits from one base class.
2. **Multiple Inheritance**: A class inherits from more than one base class.
3. **Multilevel Inheritance**: A derived class is further inherited by another class.
4. **Hierarchical Inheritance**: Multiple classes inherit from a single base class.
5. **Hybrid Inheritance**: A combination of more than one type of inheritance.

---

### **Example: Single Inheritance**
```cpp
#include <iostream>
using namespace std;

// Base class
class Vehicle {
public:
    string brand = "Ford";

    void honk() {
        cout << "Tuut, tuut!" << endl;
    }
};

// Derived class
class Car : public Vehicle {
public:
    string model = "Mustang";
};

int main() {
    Car myCar;

    // Accessing methods and attributes from the base class
    myCar.honk();
    cout << "Brand: " << myCar.brand << endl;
    cout << "Model: " << myCar.model << endl;

    return 0;
}
```

#### **Output**:
```
Tuut, tuut!
Brand: Ford
Model: Mustang
```

---

### **Access Control in Inheritance**
The **access specifier** (`public`, `protected`, `private`) used in inheritance determines how members of the base class are inherited in the derived class:

| **Base Class Member** | **Public Inheritance** | **Protected Inheritance** | **Private Inheritance** |
|------------------------|------------------------|----------------------------|--------------------------|
| Public                 | Public                | Protected                  | Private                  |
| Protected              | Protected             | Protected                  | Private                  |
| Private                | Not inherited         | Not inherited              | Not inherited            |

---

### **Example: Protected Members**
```cpp
#include <iostream>
using namespace std;

// Base class
class Animal {
protected:
    string species = "Dog";

public:
    void makeSound() {
        cout << "Woof!" << endl;
    }
};

// Derived class
class Dog : public Animal {
public:
    void showSpecies() {
        cout << "Species: " << species << endl; // Accessing protected member
    }
};

int main() {
    Dog myDog;

    myDog.makeSound();  // Accessing public member of base class
    myDog.showSpecies(); // Accessing protected member through derived class method

    return 0;
}
```

#### **Output**:
```
Woof!
Species: Dog
```

---

### **Example: Multiple Inheritance**
A class can inherit from more than one base class.

```cpp
#include <iostream>
using namespace std;

// Base class 1
class Animal {
public:
    void eat() {
        cout << "This animal eats food." << endl;
    }
};

// Base class 2
class Bird {
public:
    void fly() {
        cout << "This bird can fly." << endl;
    }
};

// Derived class
class Bat : public Animal, public Bird {
public:
    void sleep() {
        cout << "This bat sleeps during the day." << endl;
    }
};

int main() {
    Bat myBat;

    myBat.eat();   // From Animal
    myBat.fly();   // From Bird
    myBat.sleep(); // From Bat

    return 0;
}
```

#### **Output**:
```
This animal eats food.
This bird can fly.
This bat sleeps during the day.
```

---

### **Constructor and Inheritance**
When a derived class object is created, the constructor of the base class is called first, followed by the derived class constructor.

#### **Example**:
```cpp
#include <iostream>
using namespace std;

// Base class
class Animal {
public:
    Animal() {
        cout << "Animal constructor called!" << endl;
    }
};

// Derived class
class Dog : public Animal {
public:
    Dog() {
        cout << "Dog constructor called!" << endl;
    }
};

int main() {
    Dog myDog; // Calls both constructors

    return 0;
}
```

#### **Output**:
```
Animal constructor called!
Dog constructor called!
```

---

### **Key Points about Inheritance**
1. **Code Reusability**: Inheritance reduces code duplication by reusing functionality from the base class.
2. **Polymorphism**: Inheritance enables polymorphic behavior through method overriding (covered in the next section).
3. **Overriding Members**: A derived class can override base class methods.
4. **Virtual Base Classes**: In multiple inheritance, virtual base classes help avoid ambiguity and redundancy.

---
