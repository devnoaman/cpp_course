<style>
.flex-container {
    display: flex
;
    flex-wrap: nowrap;
    background-color: DodgerBlue;
    color: #000;
}

.flex-container .box {
    background-color: #f1f1f1;
    width: 50%;
    margin: 10px;
    text-align: center;
    line-height: 35px;
}
</style>


## C++: Classes and Objects

In **Object-Oriented Programming (OOP)**, **classes** and **objects** are core concepts. Let's dive into their definitions and practical examples:

---

### **What is a Class?**
A **class** is a blueprint for creating objects. It defines properties (attributes) and behaviors (methods) that the objects created from the class will have.

Think of a **class** as a template, like a design for a house. It defines the structure but doesn't create the actual house.

---

### **What is an Object?**
An **object** is an instance of a class. It represents the actual entity that has the attributes and behaviors defined in the class.

Using the house analogy, an **object** is the actual house built using the blueprint.
<div class="flex-container">
  <div class="box">
    <h2>class</h2>  
    <p>Fruit</p>
  </div>
  <div class="box">
    <h2>objects</h2>  
    <p>Apple</p>
    <p>Banana</p>
    <p>Mango</p>
  </div>
</div>


another example 
<div class="flex-container">
  <div class="box">
    <h2>class</h2>  
    <p>Car</p>
  </div>
  <div class="box">
    <h2>objects</h2>  
    <p>Volvo</p>
    <p>Audi</p>
    <p>Toyota</p>
  </div>
</div>



### Example: Class and Object

```cpp
#include <iostream>
using namespace std;

// Define a class
class Car {
public: // Access specifier (more about this later)
    string brand;  // Attribute
    string model;  // Attribute
    int year;      // Attribute

    // Method (function inside a class)
    void printDetails() {
        cout << "Brand: " << brand << ", Model: " << model << ", Year: " << year << "\n";
    }
};

int main() {
    // Create an object of Car
    Car car1;

    // Set attributes
    car1.brand = "Toyota";
    car1.model = "Corolla";
    car1.year = 2020;

    // Call a method
    car1.printDetails();

    return 0;
}
```

---

### **Access Modifiers**
Access modifiers define how the members (attributes and methods) of a class can be accessed. C++ has three access modifiers:

1. **public**: Members are accessible from outside the class.
2. **private**: Members are only accessible within the class itself.
3. **protected**: Members are accessible in the class and by derived classes.

#### Example: Access Modifiers

```cpp
#include <iostream>
using namespace std;

class Employee {
private:
    double salary; // Private attribute

public:
    string name;   // Public attribute

    // Setter method to set the private salary
    void setSalary(double s) {
        salary = s;
    }

    // Getter method to access the private salary
    double getSalary() {
        return salary;
    }
};

int main() {
    Employee emp;

    // Access and modify public attribute
    emp.name = "John Doe";

    // Use setter to assign private attribute
    emp.setSalary(50000);

    // Output
    cout << "Employee Name: " << emp.name << "\n";
    cout << "Employee Salary: $" << emp.getSalary() << "\n";

    return 0;
}
```

---

### **Constructors**
A **constructor** is a special method that is automatically called when an object is created. It initializes the object.

#### Example: Constructor

```cpp
#include <iostream>
using namespace std;

class Car {
public:
    string brand;
    string model;
    int year;

    // Constructor
    Car(string b, string m, int y) {
        brand = b;
        model = m;
        year = y;
    }

    void printDetails() {
        cout << "Brand: " << brand << ", Model: " << model << ", Year: " << year << "\n";
    }
};

int main() {
    // Create objects and initialize with constructor
    Car car1("BMW", "X5", 2019);
    Car car2("Ford", "Mustang", 2021);

    car1.printDetails();
    car2.printDetails();

    return 0;
}
```

---

### **Inheritance**
Inheritance allows a class (child class) to acquire properties and methods from another class (parent class). This promotes reusability and the DRY principle.

#### Example: Inheritance

```cpp
#include <iostream>
using namespace std;

// Base class (parent)
class Animal {
public:
    void eat() {
        cout << "This animal eats food.\n";
    }
};

// Derived class (child)
class Dog : public Animal {
public:
    void bark() {
        cout << "The dog barks.\n";
    }
};

int main() {
    Dog myDog;

    myDog.eat();  // Inherited method
    myDog.bark(); // Method from the Dog class

    return 0;
}
```

---

### **Polymorphism** تعدد الأشكال
Polymorphism allows methods in derived classes to override methods in the base class.

#### Example: Method Overriding

```cpp
#include <iostream>
using namespace std;

class Animal {
public:
    virtual void makeSound() { // Virtual function
        cout << "Animal sound\n";
    }
};

class Dog : public Animal {
public:
    void makeSound() override { // Override base class method
        cout << "Woof woof\n";
    }
};

class Cat : public Animal {
public:
    void makeSound() override {
        cout << "Meow\n";
    }
};

int main() {
    Animal* animal1 = new Dog();
    Animal* animal2 = new Cat();

    animal1->makeSound();
    animal2->makeSound();

    delete animal1;
    delete animal2;

    return 0;
}
```

---

### **Encapsulation** التغليف
Encapsulation binds the data (attributes) and methods (functions) together and restricts direct access to some components.

#### Example: Encapsulation

```cpp
#include <iostream>
using namespace std;

class BankAccount {
private:
    double balance;

public:
    // Constructor
    BankAccount(double initialBalance) {
        balance = initialBalance;
    }

    // Method to deposit money
    void deposit(double amount) {
        balance += amount;
    }

    // Method to withdraw money
    void withdraw(double amount) {
        if (amount > balance) {
            cout << "Insufficient balance.\n";
        } else {
            balance -= amount;
        }
    }

    // Method to get balance
    double getBalance() {
        return balance;
    }
};

int main() {
    BankAccount account(1000);

    account.deposit(500);
    cout << "Balance: $" << account.getBalance() << "\n";

    account.withdraw(200);
    cout << "Balance: $" << account.getBalance() << "\n";

    account.withdraw(2000); // Exceeds balance

    return 0;
}
```

---

### **Abstraction** التجريد
Abstraction focuses on hiding the implementation details and showing only the necessary features of an object.

#### Example: Abstract Class

```cpp
#include <iostream>
using namespace std;

class Shape {
public:
    virtual void draw() = 0; // Pure virtual function (abstract method)
};

class Circle : public Shape {
public:
    void draw() override {
        cout << "Drawing a Circle\n";
    }
};

class Rectangle : public Shape {
public:
    void draw() override {
        cout << "Drawing a Rectangle\n";
    }
};

int main() {
    Shape* shape1 = new Circle();
    Shape* shape2 = new Rectangle();

    shape1->draw();
    shape2->draw();

    delete shape1;
    delete shape2;

    return 0;
}
```

---

