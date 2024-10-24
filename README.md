Name: Akhilendra Pratap Singh                                            
Company: CODTECH IT SOLUTIONS                                                    
ID: CT6WDS1922                                                                          
Domain: Java Programming                                                                                                 
Duration: September to October 2024       

### **Library Management System - Project Overview**

#### **Project Introduction**
The Library Management System is a Java-based application designed to automate and simplify the process of managing books and student records in a library. It allows users to perform operations like adding new books, displaying the current catalog of books, issuing books to students, returning books, and managing student records. The system is powered by a MySQL database that stores all the necessary information, including books, students, and the book issuance status.

#### **Key Features**
1. **Book Management**
   - **Add Book**: Allows users to add a new book by entering the title and author.
   - **Display Books**: Displays all the books in the library, including their availability status (issued or available).
   - **Issue Book**: Facilitates issuing a book to a student, updating both the book's availability status and the student's record.
   - **Return Book**: Allows students to return books and updates the database to reflect the return.

2. **Student Management**
   - **Add Student**: Allows users to add new students to the system.
   - **Display Students**: Displays all students along with a list of books they have currently issued.

3. **MySQL Integration**
   - The system is integrated with a MySQL database, which contains two main tables: `books` and `students`.
   - **Books Table**: Stores the book ID, title, author, and availability (whether the book is issued or available).
   - **Students Table**: Stores student ID, name, and the list of books they have issued.

4. **User Interaction**
   - The system interacts with the user through a text-based menu, which offers different operations like adding books, displaying lists, issuing and returning books, and managing student data.

#### **Classes and Methods**

##### 1. **Main Class: `LibraryManagementSystem`**
   - This is the entry point of the system where the main method handles user interaction and calls appropriate methods for each operation.
   - **Switch-case menu**: Offers options like adding books, issuing books, displaying books, etc.

##### 2. **Database Connection**
   - This method establishes a connection to the MySQL database using `DriverManager`.
   - The database connection parameters include the URL, username, and password.

##### 3. **Database Setup**
   - This method sets up the required database tables (`books` and `students`) if they do not already exist.
   - It uses SQL `CREATE TABLE` statements to define the structure of both tables.

##### 4. **Book Management Methods**
   - **Add Book**: Adds a new book to the `books` table.
   - **Display Books**: Fetches and displays all the books from the database. Each book is shown with its ID, title, author, and availability status.
   - **Issue Book**: Issues a book to a student by updating the `isIssued` flag in the `books` table and adding the book ID to the `issuedBooks` column in the `students` table.
   - **Return Book**: Returns a book by marking it as available in the `books` table and removing the book ID from the student's issued books list.

##### 5. **Student Management Methods**
   - **Add Student**: Adds a new student to the `students` table.
   - **Display Students**: Displays all students along with the list of books they have currently issued.

#### **Database Design**
- **Books Table**
  - **id**: Auto-incremented primary key for each book.
  - **title**: Stores the book title.
  - **author**: Stores the author's name.
  - **isIssued**: Boolean field that indicates whether the book is issued or not.

- **Students Table**
  - **id**: Auto-incremented primary key for each student.
  - **name**: Stores the student’s name.
  - **issuedBooks**: A comma-separated list of book IDs representing the books currently issued by the student.

#### **SQL Queries Overview**
- **Creating Tables**: SQL queries create the `books` and `students` tables with appropriate fields.
- **Inserting Data**: SQL `INSERT` queries are used to add new books and students into their respective tables.
- **Updating Book Issuance**: SQL `UPDATE` queries handle the issuance and return of books, modifying the availability of books and the list of issued books for students.

#### **Error Handling**
- The system contains basic exception handling, where any SQL errors or connection issues are caught and the error message is printed to the console for debugging.

#### **Future Enhancements**
1. **User Authentication**: Adding a login system to differentiate between librarian and student roles.
2. **Enhanced Validation**: Improve input validation (e.g., checking if book ID and student ID exist before issuing/returning).
3. **Graphical User Interface (GUI)**: Implement a graphical interface using JavaFX or Swing for better user interaction.
4. **More Features**: Adding advanced features like book search, book categorization, and student borrowing limits.

#### **Conclusion**
This project demonstrates the core functionality of a library management system using Java and MySQL, focusing on CRUD operations for books and students. It provides a solid foundation for further enhancements and expansion, making it a practical and scalable solution for library management.
