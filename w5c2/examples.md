
---

### **1. Encapsulation**

Encapsulation hides the implementation details and protects the internal state of an object.

```cpp
#include <iostream>
using namespace std;

class Student {
private:
    string name;
    int age;
    double gpa;

public:
    // Setter methods
    void setName(string n) {
        name = n;
    }

    void setAge(int a) {
        if (a > 0) {
            age = a;
        } else {
            cout << "Invalid age!" << endl;
        }
    }

    void setGPA(double g) {
        if (g >= 0.0 && g <= 4.0) {
            gpa = g;
        } else {
            cout << "Invalid GPA!" << endl;
        }
    }

    // Getter methods
    string getName() {
        return name;
    }

    int getAge() {
        return age;
    }

    double getGPA() {
        return gpa;
    }
};

int main() {
    Student student;
    student.setName("Alice");
    student.setAge(20);
    student.setGPA(3.8);

    cout << "Student Name: " << student.getName() << endl;
    cout << "Age: " << student.getAge() << endl;
    cout << "GPA: " << student.getGPA() << endl;

    return 0;
}
```

---

### **2. Inheritance**

Inheritance enables a child class to reuse and expand the functionality of its parent class.

```cpp
#include <iostream>
using namespace std;

// Base class
class Shape {
public:
    void display() {
        cout << "This is a shape." << endl;
    }
};

// Derived class
class Circle : public Shape {
public:
    void area(double radius) {
        cout << "Area of Circle: " << 3.14 * radius * radius << endl;
    }
};

// Derived class
class Rectangle : public Shape {
public:
    void area(double length, double width) {
        cout << "Area of Rectangle: " << length * width << endl;
    }
};

int main() {
    Circle myCircle;
    Rectangle myRectangle;

    myCircle.display(); // Inherited from Shape
    myCircle.area(5.0); // Specific to Circle

    myRectangle.display(); // Inherited from Shape
    myRectangle.area(4.0, 6.0); // Specific to Rectangle

    return 0;
}
```

---

### **3. Polymorphism**

Polymorphism allows the same function to operate differently in derived classes.

```cpp
#include <iostream>
using namespace std;

// Base class
class Appliance {
public:
    virtual void turnOn() {
        cout << "Turning on the appliance." << endl;
    }
};

// Derived class
class WashingMachine : public Appliance {
public:
    void turnOn() override {
        cout << "Starting the washing cycle." << endl;
    }
};

// Derived class
class Refrigerator : public Appliance {
public:
    void turnOn() override {
        cout << "Cooling the fridge." << endl;
    }
};

int main() {
    Appliance* appliance1 = new WashingMachine();
    Appliance* appliance2 = new Refrigerator();

    appliance1->turnOn(); // Calls WashingMachine's turnOn
    appliance2->turnOn(); // Calls Refrigerator's turnOn

    delete appliance1;
    delete appliance2;

    return 0;
}
```

---

### **4. Abstraction**

Abstraction focuses on the essential features of an object by hiding unnecessary details using abstract classes.

```cpp
#include <iostream>
using namespace std;

// Abstract base class
class Employee {
public:
    virtual void calculateSalary() = 0; // Pure virtual function
};

// Derived class
class Manager : public Employee {
private:
    double baseSalary;
    double bonus;

public:
    Manager(double base, double b) : baseSalary(base), bonus(b) {}

    void calculateSalary() override {
        cout << "Manager's Salary: " << baseSalary + bonus << endl;
    }
};

// Derived class
class Engineer : public Employee {
private:
    double hourlyRate;
    int hoursWorked;

public:
    Engineer(double rate, int hours) : hourlyRate(rate), hoursWorked(hours) {}

    void calculateSalary() override {
        cout << "Engineer's Salary: " << hourlyRate * hoursWorked << endl;
    }
};

int main() {
    Employee* emp1 = new Manager(5000.0, 2000.0);
    Employee* emp2 = new Engineer(50.0, 160);

    emp1->calculateSalary(); // Calls Manager's implementation
    emp2->calculateSalary(); // Calls Engineer's implementation

    delete emp1;
    delete emp2;

    return 0;
}
```

---

