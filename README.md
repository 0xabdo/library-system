# library-system
Library Management System – Project Documentation

Project type: Console-based Python application

Submission file: library_system_abdulrahman.ipynb

1. Project Overview

The Library Management System is a console-based application that manages books and library members. It allows users to view available books, search the catalogue, add books, register members, borrow and return books, and view the books borrowed by a member. It also supports saving and loading data through JSON.

2. Development Approach

Designed separate classes so each class has a clear responsibility.

Implemented the Book class to store book details and control availability.

Implemented Member to manage borrowed books and enforce a borrowing limit.

Added PremiumMember as a subclass to demonstrate inheritance and method overriding.

Implemented Library to coordinate books and members using dictionaries keyed by unique IDs.

Created a menu-driven main() function using a while loop and conditional statements.

Added validation and exception handling to keep the program running after invalid input or file errors.

Added JSON serialization and loading to preserve the library's data between runs.

Added quick tests for successful borrowing/returning, unavailable books, duplicate IDs, and borrowing limits.

3. Classes and OOP Concepts

Class

Responsibility

OOP concept

Book

Stores book details and controls availability.

Encapsulation; __str__

Member

Stores member details and manages borrowed books.

Encapsulation; __str__

PremiumMember

Provides a higher borrowing limit.

Inheritance; polymorphism

Library

Manages books, members, lending, returns, and JSON data.

Object collaboration

4. Python Features Used

Variables, strings, lists, dictionaries, and Boolean values.

while loops and for loops.

if / elif / else conditional statements.

Functions and class methods.

try / except exception handling.

List comprehensions for searching and filtering.

File handling with open().

The json module for saving and loading structured data.

5. Python Libraries

The project uses Python's built-in json module for data persistence and pathlib.Path to represent the JSON file path. No external packages are required.

6. Validation and Edge Cases

Duplicate book IDs and member IDs are rejected.

A book that is already borrowed cannot be borrowed again.

A member cannot exceed their borrowing limit (3 for regular members and 5 for premium members).

A member cannot return a book they did not borrow.

Unknown member IDs and book IDs produce clear messages.

Empty required fields and invalid menu choices are handled.

Missing, malformed, or inaccessible JSON files are reported without terminating the menu.

7. How to Run

Open library_system_yourname.ipynb in Jupyter Notebook, VS Code, or Google Colab. Run the cells from top to bottom. Run the quick tests cell and confirm that it prints 'All quick tests passed.' Then execute main() in the final application cell to open the interactive menu.

8. Testing Checklist

☐ View available books.

☐ Search by book ID, title, and author.

☐ Add a new book and attempt a duplicate ID.

☐ Register regular and premium members and attempt a duplicate ID.

☐ Borrow an available book.

☐ Attempt to borrow an unavailable book.

☐ Borrow up to and beyond the member's limit.

☐ Return a borrowed book and attempt to return it again.

☐ View a member's borrowed books, including a member with no borrowed books.

☐ Save data, restart or reload, and confirm the records remain available.

☐ Enter invalid menu options and unknown IDs.

9. Conclusion

The project demonstrates how Python fundamentals and object-oriented programming can be combined to build a practical application. Separating responsibilities into classes makes the system easier to understand, test, and extend.
