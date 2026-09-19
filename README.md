# 🎓 University Enrollment System

### A Java OOP-Based University Management Application with a Modern Web Interface

> A practical Java application that demonstrates Object-Oriented Programming through a real-world university enrollment workflow.

![Java](https://img.shields.io/badge/Java-11%2B-blue.svg)
![Frontend](https://img.shields.io/badge/Frontend-HTML%2FCSS%2FJavaScript-orange.svg)
![Architecture](https://img.shields.io/badge/Architecture-Java%20OOP%20%2B%20HTTP-green.svg)
![Status](https://img.shields.io/badge/Status-Active-brightgreen.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

---

## 📖 About the Project

The **University Enrollment System** is a Java-based application designed to simulate a real-world university enrollment process.

The project combines **Core Java, Object-Oriented Programming, HTTP communication, and a modern web interface** to create an interactive university management workflow.

Instead of demonstrating OOP concepts individually, this project connects them together through real entities such as:

* 👨‍🎓 Students
* 👨‍🏫 Professors
* 📚 Courses
* 📝 Enrollments
* ⚠️ Enrollment Rules
* 🌐 Web Interface

The backend is developed using Java's built-in `HttpServer`, while the frontend uses HTML, CSS, and Vanilla JavaScript.

---

## 🎯 Project Objectives

The main objectives of this project are to:

* Apply Java OOP concepts to a practical problem.
* Model real-world university entities using classes.
* Demonstrate relationships between Java objects.
* Implement custom exception handling.
* Validate course enrollment capacity.
* Connect a Java backend with a browser-based frontend.
* Understand basic client-server communication.
* Build a clean and maintainable project structure.

---

# ✨ Features

### 👨‍🎓 Student Management

Create and manage student objects containing information such as:

* Student name
* Email
* Roll number
* CGPA

Each student can be associated with a course through the enrollment system.

---

### 👨‍🏫 Professor Management

Professors are represented as separate Java objects.

The system supports:

* Professor creation
* Department information
* Course assignment
* Relationship between professors and courses

---

### 📚 Course Management

Courses form the central part of the enrollment system.

Each course can maintain:

* Course name
* Course capacity
* Assigned professor
* List of enrolled students

---

### 📝 Course Enrollment

Students can enroll in available courses through the web interface.

The application checks course capacity before completing the enrollment.

```text
Student
   │
   ▼
Enrollment Request
   │
   ▼
Course Capacity Check
   │
   ├── Available ──► Enrollment Successful
   │
   └── Full ───────► EnrollmentException
```

---

### ⚠️ Custom Exception Handling

The application uses a custom exception:

```java
EnrollmentException
```

This exception is triggered when a student attempts to enroll in a course that has reached its maximum capacity.

This keeps the business rule inside the backend rather than relying only on frontend validation.

---

### 🌐 Modern Web Interface

The project includes a browser-based UI built with:

* HTML5
* CSS3
* Vanilla JavaScript
* Fetch API

The interface uses a modern **glassmorphism-inspired design** without requiring large frontend frameworks.

---

# 🧠 OOP Concepts Demonstrated

One of the primary goals of the project is to demonstrate how Java OOP concepts work together in a practical system.

---

## 🔷 1. Abstraction

`Person` acts as an abstract base class for common attributes and behavior.

```text
             Person
            /      \
           /        \
      Student      Professor
```

This allows common functionality to be defined once and reused by derived classes.

---

## 🧬 2. Inheritance

Both `Student` and `Professor` inherit from `Person`.

This represents an **IS-A relationship**:

```text
Student IS-A Person

Professor IS-A Person
```

---

## 🔒 3. Encapsulation

The classes protect their internal data and provide controlled access through appropriate methods.

```text
Private Data
     ↓
Getter / Setter
     ↓
Controlled Access
```

This helps maintain data integrity.

---

## 🔗 4. Aggregation

A `Course` maintains relationships with students and professors.

```text
             Course
             /    \
            /      \
       Professor   Students
                     │
                List<Student>
```

This demonstrates a **HAS-A relationship**.

---

## 🚨 5. Custom Exception Handling

The system defines its own:

```java
EnrollmentException
```

to represent course-capacity-related errors.

---

## 🔢 6. Static Members

Static members are used where information needs to be maintained at the class level, such as generating unique student roll numbers.

---

# 🏗️ System Architecture

The application follows a lightweight client-server architecture.

```text
┌─────────────────────────────────┐
│          Web Browser            │
│                                 │
```
