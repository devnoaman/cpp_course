### Homework: Working with Nested Structures in C++

#### Context: 
You are tasked with simulating a simple library management system using nested structures in C++. The goal is to model a library that holds multiple books, each with specific details, and perform basic operations like adding and displaying book information.

---

#### Task: Define a Nested Structure

1. **Structure Definition:**
   - Create a structure called `Book` with the following fields:
     - `title` (string): The name of the book.
     - `author` (string): The author of the book.
     - `ISBN` (string): The book's International Standard Book Number.
   - Create another structure called `Library` that contains:
     - `LibraryName` (string): The name of the library.
     - An array of `Book` with a maximum capacity of 5 books.

2. **Operations to Implement:**
   - **Input Details:**
     - Ask the user to input the library name.
     - Allow the user to add up to 5 books by providing their details (`title`, `author`, `ISBN`).
   - **Display Details:**
     - Print the name of the library.
     - Display details of all books stored in the library.
   - **Search by ISBN:**
     - Ask the user to input an ISBN.
     - Search the array of books for a match.
     - Print the details of the book if found, or display an error message if not.

---

#### Example Workflow:

**Input:**
```plaintext
Enter Library Name: City Central Library
Enter details for Book 1:
  Title: The Catcher in the Rye
  Author: J.D. Salinger
  ISBN: 9780316769488
Enter details for Book 2:
  Title: To Kill a Mockingbird
  Author: Harper Lee
  ISBN: 9780061120084
...
Enter ISBN to search: 9780316769488
```

**Output:**
```plaintext
Library Name: City Central Library

Books in Library:
1. Title: The Catcher in the Rye
   Author: J.D. Salinger
   ISBN: 9780316769488

2. Title: To Kill a Mockingbird
   Author: Harper Lee
   ISBN: 9780061120084

Search Result:
Title: The Catcher in the Rye
Author: J.D. Salinger
ISBN: 9780316769488
```

---

#### Hints:
1. Use a loop to populate the `Book` array in the `Library` structure.
2. Use conditionals and a loop to search for the ISBN in the `Book` array.
3. Implement separate functions for adding books, displaying details, and searching for a book to make the program modular.

---

