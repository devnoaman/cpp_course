

---

### **Access Specifiers in C++**
Access specifiers control the visibility and accessibility of class members (attributes and methods). In C++, there are **three access specifiers**:

1. **public**:
   - Members are accessible from **outside the class**.
   - Typically used for methods or attributes that need to interact with external code.

2. **private**:
   - Members are **not accessible from outside the class**.
   - Only accessible within the class itself.
   - Useful for encapsulating data and implementation details.

3. **protected**:
   - Similar to `private`, but with one exception:  
     Members are accessible in **derived classes** (through inheritance).

---

### **Default Access Specifier**
If no access specifier is explicitly mentioned, the default is **private**.

```cpp
class MyClass {
    int x;  // Private by default
};
```

---

### **1. Public Members**

**Public members** can be accessed directly through an object of the class.

#### Example:
```cpp
#include <iostream>
using namespace std;

class MyClass {
public:  // Public access specifier
    int x;  // Public attribute
};

int main() {
    MyClass obj;
    obj.x = 10;  // Accessible directly
    cout << "Value of x: " << obj.x << endl;  // Output: Value of x: 10
    return 0;
}
```

---

### **2. Private Members**

**Private members** are hidden from outside the class. They can only be accessed through methods within the same class.

#### Example:
```cpp
#include <iostream>
using namespace std;

class MyClass {
private:  // Private access specifier
    int y;  // Private attribute

public:
    void setY(int value) {  // Public method to set private attribute
        y = value;
    }

    int getY() {  // Public method to get private attribute
        return y;
    }
};

int main() {
    MyClass obj;

    // obj.y = 10;  // Error: y is private
    obj.setY(10);  // Set value using public method
    cout << "Value of y: " << obj.getY() << endl;  // Output: Value of y: 10

    return 0;
}
```

---

### **3. Protected Members**

**Protected members** are similar to private members but are accessible in derived classes.

#### Example:
```cpp
#include <iostream>
using namespace std;

class Base {
protected:  // Protected access specifier
    int z;

public:
    void setZ(int value) {
        z = value;
    }
};

class Derived : public Base {
public:
    void displayZ() {
        cout << "Value of z: " << z << endl;  // Accessible in derived class
    }
};

int main() {
    Derived obj;
    obj.setZ(20);  // Access through public method in Base
    obj.displayZ();  // Output: Value of z: 20
    return 0;
}
```

---

### **Comparison Table**

| **Access Specifier** | **Access Within Class** | **Access Outside Class** | **Access in Derived Class** |
|-----------------------|-------------------------|---------------------------|-----------------------------|
| **public**            | ✅                     | ✅                         | ✅                           |
| **private**           | ✅                     | ❌                         | ❌                           |
| **protected**         | ✅                     | ❌                         | ✅                           |

---

### **Best Practices**
1. **Use `private` for attributes** to enforce encapsulation:
   - Prevent direct access to data.
   - Use public methods (getters/setters) for controlled access.
2. **Use `public` for methods** that are part of the class interface.
3. Use `protected` when designing classes with inheritance in mind.

---

### **Default Private Members**

By default, all members of a class are private unless specified otherwise.

#### Example:
```cpp
#include <iostream>
using namespace std;

class MyClass {
    int x;  // Private by default
};

int main() {
    MyClass obj;
    // obj.x = 10;  // Error: x is private
    return 0;
}
```

---

