
---

# Real-Life Example: Car Rental System

In this example, we'll create a program that stores data about a car available for rental. Using descriptive variable names makes it clear what each piece of data represents, and it shows how various data types can work together in a single program.

---

## Code Example: Car Rental Data

```cpp
#include <iostream>
using namespace std;

int main() {
    // Car rental data
    int carID = 101;
    string carModel = "Toyota Camry";
    int carYear = 2020;
    float rentalPricePerDay = 55.75;
    bool isAvailable = true;

    // Print car details
    cout << "Car ID: " << carID << "\n";
    cout << "Car Model: " << carModel << "\n";
    cout << "Car Year: " << carYear << "\n";
    cout << "Rental Price per Day: $" << rentalPricePerDay << "\n";
    cout << "Available for Rent: " << (isAvailable ? "Yes" : "No") << "\n";

    return 0;
}
```

### Explanation

- **`carID`**: An integer (`int`) used as a unique identifier for each car.
- **`carModel`**: A string (`string`) to hold the car model name.
- **`carYear`**: An integer representing the manufacturing year of the car.
- **`rentalPricePerDay`**: A floating-point number (`float`) representing the rental price per day.
- **`isAvailable`**: A boolean (`bool`) that indicates whether the car is available for rent.

### Output

When the program runs, it will display:

```
Car ID: 101
Car Model: Toyota Camry
Car Year: 2020
Rental Price per Day: $55.75
Available for Rent: Yes
```

---

## Benefits of Descriptive Naming

Using clear, descriptive names like `carModel`, `rentalPricePerDay`, and `isAvailable` makes the code easy to follow and maintain. Anyone reading the program will quickly understand each variable's purpose, making it a great habit for real-life applications.

> **Activity**: Add more details, such as `int rentalDays` to track the number of days rented, and calculate the total rental cost by multiplying `rentalDays` with `rentalPricePerDay`.

Using descriptive variable names and various data types together makes for more readable, understandable code, which is essential in real-world applications!