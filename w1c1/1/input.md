
---

# C++ User Input

In C++, `cin` is used to receive input from the user. While `cout` outputs information, `cin` captures what the user types using the extraction operator (`>>`).

### Syntax
- **`cin`** utilizes the extraction operator (`>>`) to read input into a specified variable.

---

## Example: Basic User Input

In this example, we will prompt the user to enter their height in centimeters, store it in the variable `height`, and then display that value.

```cpp
#include <iostream>
using namespace std;

int main() {
    float height; 
    cout << "Enter your height in cm: ";  // Prompt the user
    cin >> height;                         // Read user input
    cout << "Your height is: " << height << " cm";  // Display the input value
    return 0;
}
```

### Explanation

1. **Declare the Variable**: `float height;` - We declare a floating-point variable to hold the user’s height.
2. **Prompt the User**: `cout << "Enter your height in cm: ";` - Displays a message prompting the user to enter their height.
3. **Read Input**: `cin >> height;` - Reads the height entered by the user and stores it in the variable `height`.
4. **Display Output**: `cout << "Your height is: " << height << " cm";` - Prints the value stored in `height`.

---

## Extended Example: Taking Multiple Inputs

Now, let's extend the example by asking the user for their favorite sport and years of playing it.

```cpp
#include <iostream>
using namespace std;

int main() {
    string favoriteSport;
    int yearsPlaying;

    cout << "What is your favorite sport? ";
    cin >> favoriteSport;

    cout << "How many years have you been playing it? ";
    cin >> yearsPlaying;

    cout << "Your favorite sport is " << favoriteSport << " and you've been playing for " << yearsPlaying << " years." << endl;
    return 0;
}
```

### Explanation

- **Multiple `cin` Statements**: We use `cin >> favoriteSport;` to capture the user's favorite sport and `cin >> yearsPlaying;` to capture how many years they've played.
- **Displaying Input**: We use `cout` to print a message that includes both the `favoriteSport` and `yearsPlaying` variables.

---

## Tips for Using `cin`

- **Handling Spaces in Input**: Remember that `cin` stops reading a string at the first space. For full-line input, use `getline(cin, variable);` instead.
- **Type Matching**: Ensure that the input type matches the variable type to avoid errors (e.g., entering text when expecting an `int`).

> **Practice**: Write a program that asks the user for their favorite book and the year it was published, then display a message that includes this information.

Using `cin` for user input is essential for creating interactive applications, enabling users to provide data that can be processed within your program!