
---

## **1. What is Abstraction?** ما هو التجريد؟
Abstraction is the process of hiding implementation details while exposing only the necessary functionality. It is achieved using:

1. **Abstract Classes** (classes with at least one pure virtual function).
2. **Interfaces** (a concept where classes only declare methods without implementation).

---

## **2. Why Use Abstraction?**
- Simplifies code by focusing on what an object does instead of how it does it.
- Promotes reusability and modular design.
- Protects sensitive parts of your codebase.

---

## **3. Creating Abstract Classes**
An **abstract class** contains at least one pure virtual function (a function declared with `= 0`).

### Example: Abstract Class for Shape
```cpp
#include <iostream>
using namespace std;

// Abstract base class
class Shape {
public:
    virtual void calculateArea() = 0; // Pure virtual function
    virtual void displayType() {
        cout << "This is a shape." << endl;
    }
};

// Derived class: Circle
class Circle : public Shape {
private:
    double radius;
public:
    Circle(double r) : radius(r) {}
    void calculateArea() override {
        cout << "Circle Area: " << 3.14 * radius * radius << endl;
    }
};

// Derived class: Rectangle
class Rectangle : public Shape {
private:
    double length, width;
public:
    Rectangle(double l, double w) : length(l), width(w) {}
    void calculateArea() override {
        cout << "Rectangle Area: " << length * width << endl;
    }
};

int main() {
    Shape* circle = new Circle(5.0);
    Shape* rectangle = new Rectangle(4.0, 6.0);

    circle->displayType();
    circle->calculateArea();

    rectangle->displayType();
    rectangle->calculateArea();

    delete circle;
    delete rectangle;

    return 0;
}
```

---

## **4. Abstraction Using Interfaces**
An **interface** is essentially a class with only pure virtual functions.

### Example: Interface for Payment Systems
```cpp
#include <iostream>
using namespace std;

// Interface
class PaymentSystem {
public:
    virtual void processPayment(double amount) = 0; // Pure virtual function
};

// Derived class: PayPal
class PayPal : public PaymentSystem {
public:
    void processPayment(double amount) override {
        cout << "Processing $" << amount << " through PayPal." << endl;
    }
};

// Derived class: Credit Card
class CreditCard : public PaymentSystem {
public:
    void processPayment(double amount) override {
        cout << "Processing $" << amount << " through Credit Card." << endl;
    }
};

int main() {
    PaymentSystem* payment1 = new PayPal();
    PaymentSystem* payment2 = new CreditCard();

    payment1->processPayment(100.0);
    payment2->processPayment(250.0);

    delete payment1;
    delete payment2;

    return 0;
}
```

---

## **5. Key Points to Remember**
1. **Abstract Classes** can have both concrete (implemented) and abstract (pure virtual) methods.
2. A class **must override all pure virtual functions** of an abstract class to be instantiated.
3. **You cannot instantiate an abstract class** directly.

---

## **6. Advanced Example: Multiple Abstraction Layers**
A real-world example with multiple abstract layers.

### Example: Notification System
```cpp
#include <iostream>
using namespace std;

// Abstract base class
class Notification {
public:
    virtual void sendNotification() = 0; // Pure virtual function
};

// Derived class: Email Notification
class EmailNotification : public Notification {
public:
    void sendNotification() override {
        cout << "Sending email notification." << endl;
    }
};

// Derived class: SMS Notification
class SMSNotification : public Notification {
public:
    void sendNotification() override {
        cout << "Sending SMS notification." << endl;
    }
};

// Manager class
class NotificationManager {
public:
    void notify(Notification* n) {
        n->sendNotification();
    }
};

int main() {
    EmailNotification email;
    SMSNotification sms;

    NotificationManager manager;
    manager.notify(&email);
    manager.notify(&sms);

    return 0;
}
```

---

## **7. Practice Challenges**
1. Create an abstract class called `Vehicle` with methods like `start()` and `stop()`. Create derived classes like `Car` and `Bike` that implement these methods differently.
2. Implement a `ReportGenerator` interface that generates reports in different formats (e.g., PDF, HTML, and CSV).
3. Build a `MediaPlayer` abstract class with methods like `play()` and `stop()`. Create derived classes for `AudioPlayer` and `VideoPlayer`.

---
