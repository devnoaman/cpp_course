### **C++ Polymorphism**

Polymorphism in C++ allows objects of different derived classes to be treated as objects of a base class. This enables one function or method to behave differently based on the object it operates on. It leverages **inheritance** and **method overriding** to achieve this behavior.

---

### **Key Concepts**

1. **Compile-Time Polymorphism**:
   - Achieved through **function overloading** or **operator overloading**.
   - Determined during compilation.

2. **Run-Time Polymorphism**:
   - Achieved through **virtual functions**.
   - Behavior is determined at runtime using **dynamic dispatch**.

---

### **Example: Function Overloading (Compile-Time Polymorphism)**

```cpp
#include <iostream>
using namespace std;

class Math {
public:
    // Function to add two integers
    int add(int a, int b) {
        return a + b;
    }

    // Function to add three integers
    int add(int a, int b, int c) {
        return a + b + c;
    }
};

int main() {
    Math math;
    cout << "Sum of 5 and 10: " << math.add(5, 10) << endl; // Calls add(int, int)
    cout << "Sum of 5, 10, and 15: " << math.add(5, 10, 15) << endl; // Calls add(int, int, int)
    return 0;
}
```

#### **Output**:
```
Sum of 5 and 10: 15
Sum of 5, 10, and 15: 30
```

---

### **Example: Virtual Functions (Run-Time Polymorphism)**

In **run-time polymorphism**, a **virtual function** is used to allow method overriding in derived classes.

```cpp
#include <iostream>
using namespace std;

// Base class
class Animal {
public:
    virtual void sound() { // Virtual function
        cout << "The animal makes a sound" << endl;
    }
};

// Derived class
class Dog : public Animal {
public:
    void sound() override { // Overriding base class function
        cout << "The dog says: bow wow" << endl;
    }
};

// Derived class
class Cat : public Animal {
public:
    void sound() override {
        cout << "The cat says: meow" << endl;
    }
};

int main() {
    Animal* animal1;      // Base class pointer
    Dog dog;
    Cat cat;

    animal1 = &dog;       // Pointing to a Dog object
    animal1->sound();     // Calls Dog's sound method

    animal1 = &cat;       // Pointing to a Cat object
    animal1->sound();     // Calls Cat's sound method

    return 0;
}
```

#### **Output**:
```
The dog says: bow wow
The cat says: meow
```

---

### **Key Points about Virtual Functions**
1. **Declared using the `virtual` keyword** in the base class.
2. Allows derived classes to override the base class method.
3. Requires a base class pointer or reference to invoke overridden methods.
4. Use `override` in derived classes to indicate that a method overrides a base class method explicitly.

---

### **Abstract Classes and Pure Virtual Functions**
An **abstract class** is a class that cannot be instantiated. It contains **pure virtual functions**, which are functions that must be overridden in derived classes.

#### **Syntax for Pure Virtual Functions**:
```cpp
virtual void functionName() = 0; // Pure virtual function
```

#### **Example: Abstract Class**
```cpp
#include <iostream>
using namespace std;

// Abstract base class
class Animal {
public:
    virtual void sound() = 0; // Pure virtual function
};

// Derived class
class Dog : public Animal {
public:
    void sound() override {
        cout << "The dog says: bow wow" << endl;
    }
};

// Derived class
class Cat : public Animal {
public:
    void sound() override {
        cout << "The cat says: meow" << endl;
    }
};

int main() {
    Animal* animal1 = new Dog();
    Animal* animal2 = new Cat();

    animal1->sound(); // Calls Dog's sound method
    animal2->sound(); // Calls Cat's sound method

    delete animal1;
    delete animal2;

    return 0;
}
```

#### **Output**:
```
The dog says: bow wow
The cat says: meow
```

---

### **Benefits of Polymorphism**

1. **Code Reusability**:
   - Base class methods and attributes can be reused in derived classes.
2. **Flexibility**:
   - Allows behavior to be extended or modified in derived classes without changing the base class.
3. **Scalability**:
   - Enables design patterns like the Factory Pattern or Strategy Pattern.

---

### **When to Use Polymorphism**
- To design flexible and reusable code.
- When dealing with a group of related objects (e.g., different shapes in a drawing application).
- In scenarios where you need to decide the behavior of a class at runtime.

