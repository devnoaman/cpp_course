```markdown
# C++ Math

C++ provides a variety of functions to perform mathematical operations on numbers. Some of these functions are built-in, while others require the `<cmath>` library.

## Max and Min Functions

The `max(x, y)` function returns the highest value between `x` and `y`, while `min(x, y)` returns the lowest value.

### Example
```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Max of 5 and 10: " << max(5, 10) << "\n";
    cout << "Min of 5 and 10: " << min(5, 10);
    return 0;
}
```

Output:
```
Max of 5 and 10: 10
Min of 5 and 10: 5
```

## C++ `<cmath>` Library

To access additional mathematical functions, include the `<cmath>` library. Some commonly used functions are:

- `sqrt(x)`: Returns the square root of `x`.
- `round(x)`: Rounds `x` to the nearest integer.
- `log(x)`: Returns the natural logarithm of `x`.

### Example
```cpp
#include <iostream>
#include <cmath>
using namespace std;

int main() {
    cout << "Square root of 64: " << sqrt(64) << "\n";
    cout << "Round 2.6: " << round(2.6) << "\n";
    cout << "Natural log of 2: " << log(2);
    return 0;
}
```

Output:
```
Square root of 64: 8
Round 2.6: 3
Natural log of 2: 0.693147
```

---

## Complete Math Reference

For more math functions available in C++, consult a C++ Math Reference guide.
```
https://www.w3schools.com/cpp/cpp_ref_math.asp
```