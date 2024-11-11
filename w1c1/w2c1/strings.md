

```markdown
# C++ Strings

## 1. Strings Intro

An introduction to using strings in C++. Strings are sequences of characters, used for storing text. To work with strings, include the `<string>` library.

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string greeting = "Hello, World!";
    cout << greeting;
    return 0;
}
```

## 2. Concatenation

String concatenation combines two or more strings into one. This can be done with the `+` operator.

```cpp
string firstName = "John";
string lastName = "Doe";
string fullName = firstName + " " + lastName; // "John Doe"
cout << fullName;
```

## 3. Numbers and Strings

Combining numbers and strings requires converting numbers to strings first. Use `to_string()` for conversion.

```cpp
int age = 30;
string ageText = "Age: " + to_string(age);
cout << ageText;
```

## 4. String Length

The length of a string can be found using the `.length()` or `.size()` function.

```cpp
string text = "Hello";
cout << "Length: " << text.length();
```

## 5. Access Strings

You can access individual characters in a string by using an index.

```cpp
string word = "Hello";
cout << "First character: " << word[0];
```

## 6. Special Characters

Special characters in strings include `\n` (new line), `\t` (tab), `\"` (double quote), etc.

```cpp
string text = "He said, \"Hello!\"\n";
cout << text;
```

## 7. User Input Strings

To get string input from the user, use `cin` for single-word input and `getline(cin, variable)` for multi-word input.

```cpp
string name;
cout << "Enter your name: ";
getline(cin, name);
cout << "Hello, " << name << "!";
```

## 8. Omitting Namespace

If you don’t want to use `using namespace std;`, prefix `std::` before `string`, `cout`, and other standard library elements.

```cpp
std::string greeting = "Hello";
std::cout << greeting;
```

## 9. C-Style Strings

C-style strings are arrays of characters ending with a null character `\0`. They are used in C and supported in C++.

```cpp
char cString[] = "Hello";
cout << cString;
```

---

