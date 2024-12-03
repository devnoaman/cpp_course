```cpp
#include <iostream>
using namespace std;

int main() {
    // **Real-Life Example 1: Calculate Average Age**

    // An array storing different ages
    int ages[8] = {20, 22, 18, 35, 48, 26, 87, 70};

    float avg, sum = 0;

    // Get the length of the array
    int length = sizeof(ages) / sizeof(ages[0]);

    // Loop through the elements of the array
    for (int age : ages) {
        sum += age;
    }

    // Calculate the average by dividing the sum by the length
    avg = sum / length;

    // Print the average
    cout << "The average age is: " << avg << "\n";

    // **Real-Life Example 2: Find the Lowest Age**

    // Create a variable and assign the first array element of ages to it
    int lowestAge = ages[0];

    // Loop through the elements of the ages array to find the lowest age
    for (int age : ages) {
        if (lowestAge > age) {
            lowestAge = age;
        }
    }

    // Print the lowest age
    cout << "The lowest age is: " << lowestAge << "\n";

    return 0;
}
```

---

### **Explanation**

#### **1. Calculate Average Age**
- **Purpose:** Calculate the average age of a group of people using an array.
- **Steps:**
  1. Initialize an array (`ages`) with sample age data.
  2. Use `sizeof()` to calculate the length of the array.
  3. Iterate through the array using a `for-each` loop to sum up the ages.
  4. Compute the average by dividing the sum by the number of elements.
  5. Output the average.

#### **2. Find the Lowest Age**
- **Purpose:** Determine the youngest age in the dataset.
- **Steps:**
  1. Assign the first element of the array to `lowestAge`.
  2. Loop through the array and compare each value with `lowestAge`.
  3. Update `lowestAge` if a smaller value is found.
  4. Output the lowest age.

---

### **Sample Output**
```
The average age is: 40.75
The lowest age is: 18
```
---
---
Here's an example of using a loop, `cin`, `cout`, and an array in C++:

```cpp
#include <iostream>
using namespace std;

int main() {
    const int size = 5;
    int numbers[size];

    // Input: Prompting the user to enter values into the array
    cout << "Enter " << size << " numbers:" << endl;
    for (int i = 0; i < size; ++i) {
        cout << "Number " << (i + 1) << ": ";
        cin >> numbers[i];
    }

    // Output: Displaying the array's contents
    cout << "\nYou entered:" << endl;
    for (int i = 0; i < size; ++i) {
        cout << "numbers[" << i << "] = " << numbers[i] << endl;
    }

    return 0;
}
```

### Explanation:
1. **Array**: The `numbers` array stores integers with a fixed size of 5.
2. **`cin`**: Used to take user input for each element of the array.
3. **`cout`**: Displays messages and the contents of the array.
4. **Loop**: A `for` loop iterates through the array for both input and output.

### Example Output:
```
Enter 5 numbers:
Number 1: 10
Number 2: 20
Number 3: 30
Number 4: 40
Number 5: 50

You entered:
numbers[0] = 10
numbers[1] = 20
numbers[2] = 30
numbers[3] = 40
numbers[4] = 50
```

---
---
Here are three distinct examples with unique contexts:

---

### Example 1: Find the Maximum Element in an Array
```cpp
#include <iostream>
using namespace std;

int main() {
    const int size = 6;
    int numbers[size];

    // Input: Reading array elements
    cout << "Enter " << size << " numbers:" << endl;
    for (int i = 0; i < size; ++i) {
        cin >> numbers[i];
    }

    // Processing: Finding the maximum
    int max = numbers[0];
    for (int i = 1; i < size; ++i) {
        if (numbers[i] > max) {
            max = numbers[i];
        }
    }

    // Output: Displaying the maximum value
    cout << "The maximum number is: " << max << endl;

    return 0;
}
```

---

### Example 2: Reverse an Array
```cpp
#include <iostream>
using namespace std;

int main() {
    const int size = 5;
    int numbers[size];

    // Input: Reading array elements
    cout << "Enter " << size << " numbers:" << endl;
    for (int i = 0; i < size; ++i) {
        cin >> numbers[i];
    }

    // Output: Displaying the array in reverse order
    cout << "Array in reverse order:" << endl;
    for (int i = size - 1; i >= 0; --i) {
        cout << numbers[i] << " ";
    }
    cout << endl;

    return 0;
}
```

---

### Example 3: Count Odd and Even Numbers in an Array
```cpp
#include <iostream>
using namespace std;

int main() {
    const int size = 7;
    int numbers[size];
    int oddCount = 0, evenCount = 0;

    // Input: Reading array elements
    cout << "Enter " << size << " numbers:" << endl;
    for (int i = 0; i < size; ++i) {
        cin >> numbers[i];
    }

    // Processing: Counting odd and even numbers
    for (int i = 0; i < size; ++i) {
        if (numbers[i] % 2 == 0) {
            evenCount++;
        } else {
            oddCount++;
        }
    }

    // Output: Displaying the counts
    cout << "Even numbers count: " << evenCount << endl;
    cout << "Odd numbers count: " << oddCount << endl;

    return 0;
}
```