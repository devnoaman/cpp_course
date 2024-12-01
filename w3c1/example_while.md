```markdown
# C++ While Loop Examples

## Example 1: Countdown Program
This program demonstrates a simple countdown, ending with "Happy New Year!!".

```cpp
#include <iostream>
using namespace std;

int main() {
    int countdown = 3;

    while (countdown > 0) {
        cout << countdown << "\n"; // Print the current countdown value
        countdown--;               // Decrement countdown
    }

    cout << "Happy New Year!!\n"; // Celebration message
    return 0;
}
// Output:
// 3
// 2
// 1
// Happy New Year!!
```

---

## Example 2: Print Even Numbers
This program prints all even numbers between 0 and 10 (inclusive).

```cpp
#include <iostream>
using namespace std;

int main() {
    int i = 0;

    while (i <= 10) {
        cout << i << "\n"; // Print the current value of i
        i += 2;            // Increment by 2 to get the next even number
    }

    return 0;
}
// Output:
// 0
// 2
// 4
// 6
// 8
// 10
```

---

## Example 3: Reverse a Number
This program reverses the digits of a number.

```cpp
#include <iostream>
using namespace std;

int main() {
    int numbers = 12345;    // Original number
    int revNumbers = 0;     // Variable to store the reversed number

    while (numbers) {
        revNumbers = revNumbers * 10 + numbers % 10; // Add the last digit to reversed number
        numbers /= 10;                              // Remove the last digit
    }

    cout << "Reversed numbers: " << revNumbers << "\n";
    return 0;
}
// Output:
// Reversed numbers: 54321
```

---

## Example 4: Yatzy Game Simulation
This program simulates a simplified Yatzy game.

```cpp
#include <iostream>
using namespace std;

int main() {
    int dice = 1;

    while (dice <= 6) {
        if (dice < 6) {
            cout << "No Yatzy\n"; // Not a winning roll
        } else {
            cout << "Yatzy!\n";   // Winning roll
        }
        dice = dice + 1;          // Increment dice value
    }

    return 0;
}
// Output:
// No Yatzy
// No Yatzy
// No Yatzy
// No Yatzy
// No Yatzy
// Yatzy!
```

--- 
```