# Library Management System:

You are tasked with building a **Library Management System** using JavaScript to help a local library manage its books, members, and borrowing transactions. The system should allow the library to perform various operations such as adding books, registering members, borrowing and returning books, and generating reports.

### Requirements

#### 1. Book Management
- Each book object should be of the following format:
  - `id` (unique identifier),
  - `title` (string),
  - `author` (string),
  - `genre` (string),
  - `totalCopies` (number),
  - `availableCopies` (number).
- Implement functions to:
  - Add a new book to the library.
  - Remove a book by its ID (only if no copies are borrowed).
  - Search for books by title or author.
  - Display all books in a specific genre.

#### 2. Member Management
- Each member object be of the following format:
  - `memberId` (unique identifier),
  - `name` (string),
  - `email` (string),
  - `borrowedBooks` (array of objects containing `bookId` and `borrowDate`).
- Implement functions to:
  - Register a new member.
  - Remove a member by their ID (only if they have no borrowed books).
  - Display all members who have borrowed at least one book.

#### 3. Borrowing and Returning
- Implement functions to:
  - Allow a member to borrow a book (update `availableCopies` and add to `borrowedBooks`).
  - Allow a member to return a book (update `availableCopies` and remove from `borrowedBooks`).
  - Prevent borrowing if:
    - The book is not available.
    - The member already has 3 borrowed books (library policy).
  - Prevent returning a book that the member hasn’t borrowed.
  - note: Do check all the corner cases.

#### 4. Reports
- Generate a report of all books that are currently borrowed (include book title and borrowing member’s name).
- Find the most popular genre (based on the number of books borrowed in that genre).
- List all members who have overdue books (assume a book is overdue if it’s been borrowed for more than 14 days).

#### 5. Must To Do
- Use what you've learnt in the past two weeks to implement this project.