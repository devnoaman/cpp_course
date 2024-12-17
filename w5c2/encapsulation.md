### **C++ Encapsulation**

Encapsulation is a fundamental concept in object-oriented programming (OOP) that helps to bundle data and the methods that operate on that data into a single unit (class). It restricts direct access to some of the object's components, thereby improving code security and maintainability.

---

### **Key Features of Encapsulation**
1. **Data Hiding**: Keeps sensitive data hidden from the outside world.
2. **Controlled Access**: Provides public methods (getters and setters) to access and modify private attributes.
3. **Improved Security**: Reduces the risk of accidental data corruption.
4. **Modularity**: Allows changes to implementation without affecting external code.

---

### **Accessing Private Members with Getters and Setters**

Private members cannot be accessed directly. Instead, we use **getters** (to retrieve data) and **setters** (to modify data).

#### **Example**:
```cpp
#include <iostream>
using namespace std;

class Employee {
private:
    // Private attribute
    int salary;

public:
    // Setter: Sets the value of the salary
    void setSalary(int s) {
        if (s >= 0) {  // Validation to ensure a non-negative salary
            salary = s;
        } else {
            cout << "Salary cannot be negative!" << endl;
        }
    }

    // Getter: Returns the value of the salary
    int getSalary() {
        return salary;
    }
};

int main() {
    Employee emp;

    emp.setSalary(50000);  // Setting the salary
    cout << "Employee salary: " << emp.getSalary() << endl;

    emp.setSalary(-100);  // Attempting to set an invalid salary
    cout << "Updated salary: " << emp.getSalary() << endl;

    return 0;
}
```

#### **Output**:
```
Employee salary: 50000
Salary cannot be negative!
Updated salary: 50000
```

---

### **Why Use Encapsulation?**

1. **Better Control of Data**:
   - You can validate data within setter methods (as seen in the example above).
   - Protects against invalid or inconsistent data.

2. **Flexibility for Future Changes**:
   - Changes to the internal implementation of a class do not affect external code using that class.

3. **Data Security**:
   - By hiding sensitive attributes, the risk of accidental or malicious modification is reduced.

4. **Modular Code**:
   - Encapsulation divides the program into small, self-contained modules (classes), making it easier to understand, test, and debug.

---

### **Example with Multiple Attributes**

```cpp
#include <iostream>
using namespace std;

class Car {
private:
    string brand;
    int year;
    int speed;

public:
    // Setter for brand
    void setBrand(string b) {
        brand = b;
    }

    // Getter for brand
    string getBrand() {
        return brand;
    }

    // Setter for year
    void setYear(int y) {
        if (y > 1885) {  // Ensuring a valid year for car production
            year = y;
        } else {
            cout << "Invalid year!" << endl;
        }
    }

    // Getter for year
    int getYear() {
        return year;
    }

    // Setter for speed
    void setSpeed(int s) {
        if (s >= 0) {
            speed = s;
        } else {
            cout << "Speed cannot be negative!" << endl;
        }
    }

    // Getter for speed
    int getSpeed() {
        return speed;
    }
};

int main() {
    Car car;

    car.setBrand("Tesla");
    car.setYear(2023);
    car.setSpeed(120);

    cout << "Car details:\n";
    cout << "Brand: " << car.getBrand() << endl;
    cout << "Year: " << car.getYear() << endl;
    cout << "Speed: " << car.getSpeed() << " km/h" << endl;

    car.setSpeed(-50);  // Invalid speed
    cout << "Updated Speed: " << car.getSpeed() << " km/h" << endl;

    return 0;
}
```

#### **Output**:
```
Car details:
Brand: Tesla
Year: 2023
Speed: 120 km/h
Speed cannot be negative!
Updated Speed: 120 km/h
```

---

### **Advantages of Encapsulation**
1. **Code Reusability**: Encapsulated code can be reused across different parts of the program.
2. **Ease of Testing**: Encapsulation simplifies unit testing by isolating each class.
3. **Better Debugging**: Encapsulated data reduces the chances of unexpected side effects caused by external changes.
4. **Enhanced Maintenance**: Encapsulated classes are easier to maintain and modify as they expose only controlled access points.

---

### **Common Practices**
- **Declare attributes as `private`** or `protected`.  
- **Provide `public` getters and setters** for controlled access.  
- Use **meaningful method names** for getters and setters (e.g., `setSpeed` or `getSalary`).
- Implement **validation logic** inside setter methods to ensure data consistency.  
