# Bildungsinstitute
This project is a Java-based application designed to manage courses, students, employees, and their associations within an educational institute.
The application interacts with a database to store and manage data related to courses, students, employees, and their relationships.

## Project Structure

The project is organized into several packages, each responsible for different functionalities:

1. **`com.bildungsinstitut.database`**: Contains classes responsible for database interactions, including CRUD operations for courses, students, employees, and their associations.
2. **`com.bildungsinstitut.management`**: Contains a generic class for managing entities like courses and students within the application.
3. **`com.bildungsinstitut.model`**: Defines the data models for entities such as `Course`, `Student`, `Employee`, and their relationships.
4. **`com.bildungsinstitut.util`**: Utility classes for generating unique IDs and validating input data.
5. **`com.bildungsinstitut.view`**: Contains the controller classes responsible for handling the user interface logic, connecting the frontend with the backend.

## Key Classes and Functions

### Database Classes

- **`CourseData`**: Handles CRUD operations for courses, including adding, updating, deleting, and retrieving courses from the database.
- **`StudentData`**: Manages CRUD operations for students, including the ability to remove a student and their associations with courses.
- **`EmployeeData`**: Manages CRUD operations for employees.
- **`CourseWithStudentData`**: Manages associations between courses and students.

### Management Classes

- **`InstitutionManagement<T>`**: A generic management class that provides functionalities to add, remove, update, and check for the existence of entities such as courses and students.

### Model Classes

- **`Course`**: Represents a course with properties like `id`, `name`, and `trainerID`.
- **`Student`**: Represents a student with properties like `id`, `name`, `age`, and `email`.
- **`Employee`**: Represents an employee with properties like `id`, `name`, `age`, `email`, and `position`.
- **`CourseWithStudent`**: Represents the relationship between a course and a student.

### Utility Classes

- **`UniqueID`**: Generates unique IDs for different entities within the application.
- **`ValidationUtil`**: Contains methods to validate inputs such as course names, student details, and employee details.

### View Classes

- **`CourseWindowController`**: Manages the course view, allowing users to add, update, and delete courses, as well as enroll students in courses.
- **`EmployeeWindowController`**: Manages the employee view, allowing users to add, update, and delete employees.
- **`StudentWindowController`**: Manages the student view, allowing users to add, update, and delete students.
- **`HomeWindowController`**: Manages the main dashboard view, displaying courses and their associated students and trainers.
- **`MainWindowController`**: Manages the main application window, allowing users to navigate between different sections of the application.

## How to Run

### Prerequisites

- Java Development Kit (JDK) 8 or higher
- MySQL or any compatible relational database
- JavaFX library

### Setup

1. **Database Setup**: Create a MySQL database and tables for `student`, `course`, `employee`, and `student_course`. The SQL scripts for creating these tables should be defined as per your database schema.

2. **Configure Database Connection**: Update the `DatabaseConnection` class with your database credentials (URL, username, and password).

3. **Running the Application**:
   - Compile the project using your preferred IDE or command line.
   - Run the `Main` class, which will launch the JavaFX application.

### Usage

- **Courses**: Add, update, and delete courses. You can also assign trainers (employees) to courses.
- **Students**: Add, update, and delete students. Students can be enrolled in courses.
- **Employees**: Add, update, and delete employees who can act as trainers for courses.
- **Dashboard**: View all courses and their associated students and trainers.

## Technologies Used

- **Java**: Core programming language.
- **JavaFX**: For building the graphical user interface.
- **JDBC**: For database connectivity.
- **MySQL**: As the database for storing the application's data.

