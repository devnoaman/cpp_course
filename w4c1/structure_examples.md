
---

## Example 1: Representing a Book

```cpp
#include <iostream>
using namespace std;

struct Book {
    string title;
    string author;
    int yearPublished;
    double price;
};

int main() {
    // Create a Book variable
    Book book1;

    // Assign values
    book1.title = "1984";
    book1.author = "George Orwell";
    book1.yearPublished = 1949;
    book1.price = 9.99;

    // Output the book details
    cout << "Title: " << book1.title << "\n";
    cout << "Author: " << book1.author << "\n";
    cout << "Year Published: " << book1.yearPublished << "\n";
    cout << "Price: $" << book1.price << "\n";

    return 0;
}
```

---

## Example 2: Nested Structures

```cpp
#include <iostream>
using namespace std;

// Define a nested structure
struct Address {
    string street;
    string city;
    int zipCode;
};

struct Person {
    string name;
    int age;
    Address address; // Nested structure
};

int main() {
    // Create a Person variable
    Person person1;

    // Assign values
    person1.name = "John Doe";
    person1.age = 28;
    person1.address.street = "123 Main St";
    person1.address.city = "Springfield";
    person1.address.zipCode = 12345;

    // Output the person's details
    cout << "Name: " << person1.name << "\n";
    cout << "Age: " << person1.age << "\n";
    cout << "Address: " << person1.address.street << ", " 
         << person1.address.city << ", " 
         << person1.address.zipCode << "\n";

    return 0;
}
```

---

## Example 3: Array of Structures

```cpp
#include <iostream>
using namespace std;

struct Student {
    string name;
    int grade;
    double gpa;
};

int main() {
    // Array of structures
    Student students[3];

    // Assign values to the array
    students[0] = {"Alice", 10, 3.8};
    students[1] = {"Bob", 11, 3.5};
    students[2] = {"Charlie", 12, 3.9};

    // Output student details
    for (int i = 0; i < 3; i++) {
        cout << "Name: " << students[i].name 
             << ", Grade: " << students[i].grade 
             << ", GPA: " << students[i].gpa << "\n";
    }

    return 0;
}
```

---

## Example 4: Function with Structure as a Parameter

```cpp
#include <iostream>
using namespace std;

struct Rectangle {
    double length;
    double width;
};

// Function to calculate the area of a rectangle
double calculateArea(Rectangle rect) {
    return rect.length * rect.width;
}

int main() {
    // Create a Rectangle variable
    Rectangle rect1 = {5.0, 3.0};

    // Calculate and output the area
    cout << "Area of rectangle: " << calculateArea(rect1) << "\n";

    return 0;
}
```

---

## Example 5: Returning a Structure from a Function

```cpp
#include <iostream>
using namespace std;

struct Circle {
    double radius;
    double area;
};

// Function to create and return a Circle structure
Circle createCircle(double r) {
    Circle c;
    c.radius = r;
    c.area = 3.14159 * r * r;
    return c;
}

int main() {
    // Create a Circle using the function
    Circle myCircle = createCircle(5.0);

    // Output the circle's details
    cout << "Radius: " << myCircle.radius << "\n";
    cout << "Area: " << myCircle.area << "\n";

    return 0;
}
```

---

## Example 6: Using Structures to Represent Complex Data (Employee)

```cpp
#include <iostream>
using namespace std;

struct Employee {
    int id;
    string name;
    double salary;
    string department;
};

int main() {
    // Create an Employee
    Employee emp1 = {101, "Jane Smith", 55000.50, "Engineering"};
    Employee emp2 = {102, "John Doe", 60000.75, "Marketing"};

    // Output employee details
    cout << "Employee ID: " << emp1.id << "\n"
         << "Name: " << emp1.name << "\n"
         << "Salary: $" << emp1.salary << "\n"
         << "Department: " << emp1.department << "\n\n";

    cout << "Employee ID: " << emp2.id << "\n"
         << "Name: " << emp2.name << "\n"
         << "Salary: $" << emp2.salary << "\n"
         << "Department: " << emp2.department << "\n";

    return 0;
}
```

---

## Example 7: Passing Structure by Reference

```cpp
#include <iostream>
using namespace std;

struct Point {
    int x;
    int y;
};

// Function to modify a point's coordinates
void movePoint(Point &p, int dx, int dy) {
    p.x += dx;
    p.y += dy;
}

int main() {
    // Create a Point
    Point pt = {2, 3};

    // Move the point
    movePoint(pt, 5, -1);

    // Output the new coordinates
    cout << "New coordinates: (" << pt.x << ", " << pt.y << ")\n";

    return 0;
}
```

---

## Example 8: Default Initialization with a Structure

```cpp
#include <iostream>
using namespace std;

struct Product {
    string name = "Unknown";
    double price = 0.0;
    int quantity = 0;
};

int main() {
    // Create a Product with default values
    Product defaultProduct;

    // Create a Product with specified values
    Product specificProduct = {"Laptop", 999.99, 5};

    // Output product details
    cout << "Default Product: " << defaultProduct.name 
         << ", $" << defaultProduct.price 
         << ", Quantity: " << defaultProduct.quantity << "\n";

    cout << "Specific Product: " << specificProduct.name 
         << ", $" << specificProduct.price 
         << ", Quantity: " << specificProduct.quantity << "\n";

    return 0;
}
```

---

These examples cover a range of scenarios demonstrating how structures can be used effectively in C++ programs. From simple grouping of related data to more complex operations like passing structures to functions or nesting them, structures are a powerful feature in C++.