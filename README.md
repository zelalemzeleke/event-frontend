MyLibrary - C# Desktop Library Management Application

Overview:

MyLibrary is a Windows desktop application developed using the C# programming language and the .NET Windows Forms framework. It was created as an individual assignment for the course "Event-Driven Programming with C#." The application allows a small library to manage its collection of books, track borrowers, and handle the issuing and returning of books, all with full integration into a relational database.

The application demonstrates key programming concepts such as event-driven programming, user interface design, database connectivity with ADO.NET, input validation, and exception handling.

Key Features:

Login System:
The application starts with a simple login screen where users must enter a valid username and password. These credentials are checked against records stored in the Users table in the database. If the login is successful, the user is taken to the main application window. If the credentials are incorrect, an error message is displayed.

Main Application Window:
Once logged in, the user is presented with a tabbed interface containing two main sections:

Book Management

Borrower Management

Book Management Section:
This section allows users to manage the library’s book inventory. All books are listed in a data grid that displays key information such as Book ID, Title, Author, Year of publication, and the number of available copies.

Functionalities include:

Adding a new book by entering all necessary details into a form.

Editing the details of an existing book by selecting it from the list.

Deleting a book with a confirmation prompt to prevent accidental removals.

The system validates all inputs, ensuring that text fields are not left empty and numeric fields such as year and available copies contain valid data.

Borrower Management Section:
This section lists all registered borrowers and allows for managing their information. The DataGridView displays fields such as Borrower ID, Name, Email, and Phone number.

Functionalities include:

Adding a new borrower.

Editing an existing borrower’s information.

Deleting a borrower from the database.

The application ensures that inputs are validated, including checking that emails are correctly formatted and required fields are filled.

Book Issuing and Returning:
The system allows staff to issue books to borrowers and record the transaction. When a book is issued:

The number of available copies for that book is reduced.

A new record is inserted into the IssuedBooks table, capturing details such as Book ID, Borrower ID, the date the book was issued, and the due date.

To return a book:

The issued record is selected.

The system increases the available copies for the book.

The record is either removed or marked as returned.
