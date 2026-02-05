# University Enrollment System (OOPS – Java)

## Project Overview
The University Enrollment System is a Java-based console application developed to demonstrate core Object-Oriented Programming (OOP) concepts as taught in class.  
The project models a real-world university environment involving Students, Professors, Courses, and Enrollment rules.

This project is designed strictly according to classroom discussions and syllabus requirements, covering IS-A and HAS-A relationships, inheritance, encapsulation, aggregation, and custom exception handling.

---

## Technologies Used
- Java (Core Java)
- Object-Oriented Programming (OOP)
- IntelliJ IDEA (IDE)

---

## Project Structure
University_Enrollment_System/
│

├── .idea/

│        ├── misc.xml

│        ├── modules.xml

│        └── vcs.xml

│        

├── src/

│   └──  University_Enrollment_System/

│        ├── Main.java

│        ├── Person.java

│        ├── Student.java

│        ├── Professor.java

│        ├── Course.java

│        └── EnrollmentException.java

│

├── LICENSE

├── README.md

└── oops_java_project.iml

---

## Class Description

### Person
- Base class for Student and Professor
- Contains common attributes:
  - name
  - email
- Demonstrates data abstraction

### Student
- Inherits from Person (IS-A relationship)
- Attributes:
  - rollNo (unique, auto-incremented using static variable)
  - cgpa
- Demonstrates encapsulation and data security

### Professor
- Inherits from Person (IS-A relationship)
- Assigned to courses
- Demonstrates hierarchical inheritance

### Course
- Demonstrates HAS-A relationship (Aggregation)
- Attributes:
  - course name
  - course code
  - assigned professor
  - list of enrolled students
  - maximum capacity
- Handles student enrollment logic

### EnrollmentException
- Custom exception class
- Thrown when course capacity is exceeded

### Main
- Entry point of the application
- Demonstrates object creation, method invocation, and exception handling

---

## OOP Relationships Used

### IS-A Relationship (Inheritance)
- Student extends Person
- Professor extends Person

### HAS-A Relationship (Aggregation)
- Course has Student
- Course has Professor

---

## Syllabus Mapping

## Unit 1: OOP Basics

### Topics Covered
- Class and Object creation
- Constructors (parameterized)
- Attributes and instance variables
- Methods and method invocation
- Reference variables

### Implementation in Project
- Each entity is implemented as a separate class
- Objects are created in Main.java
- Constructors initialize object data
- Methods are used to enroll students and assign professors

---

## Unit 2: Encapsulation, Abstraction & Static Members

### Topics Covered
- Encapsulation using private variables
- Getter methods
- Static variables and methods
- Aggregation and dependency between classes

### Implementation in Project
- Student roll number is private and accessed using methods
- Static variable used for auto-increment of roll number
- Course aggregates Student and Professor objects

---

## Unit 3: Inheritance & Exception Handling

### Topics Covered
- Single and hierarchical inheritance
- Method inheritance from parent class
- Custom exception handling
- Throw and catch mechanisms
- Collection of objects with exception handling

### Implementation in Project
- Student and Professor inherit from Person
- EnrollmentException is a custom exception
- Exception is thrown when course capacity is full
- try-catch blocks used in Main.java
- Course maintains a collection of enrolled students

---

## How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/adityasahani001/University_Enrollment_System.git
   
2. Open the project in IntelliJ IDEA
3. Run Main.java

### Learning Outcomes
Understanding of OOP principles
Clear use of inheritance and aggregation
Hands-on experience with exception handling
Real-world modeling using Java

## Author
**Aditya Sahani**  
B.Tech CSE (AI/ML)  
IILM University  

- GitHub: https://github.com/adityasahani001  
- LinkedIn: https://www.linkedin.com/in/aditya-sahani-0955b02ab/

---

## Note
This project is developed for academic and learning purposes as per university syllabus.
