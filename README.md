# 🎓 University Enrollment System (Java OOP + Web UI)

> A modern, object-oriented Java application featuring a beautiful HTML/CSS Web UI, simulating a real-world university enrollment workflow.

![Java Version](https://img.shields.io/badge/Java-11%2B-blue.svg)
![Build](https://img.shields.io/badge/Build-Passing-brightgreen.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

---

## 📖 Project Overview

The **University Enrollment System** is a robust Java-based application developed to demonstrate core **Object-Oriented Programming (OOP)** concepts. The project accurately models a university environment involving **Students**, **Professors**, **Courses**, and strict **Enrollment Rules**.

This application covers essential topics including:

* **Inheritance** — IS-A relationships
* **Aggregation** — HAS-A relationships
* **Encapsulation & Data Hiding**
* **Custom Exception Handling**

---

## ✨ Features

* 👨‍🎓 **Student Management**
  Register students with unique IDs, emails, and CGPAs.

* 👨‍🏫 **Professor Allocation**
  Assign professors to specific departments and courses.

* 📚 **Course Enrollment**
  Enroll students into courses with defined capacities.

* ⚠️ **Custom Error Handling**
  Prevent over-enrollment using the custom `EnrollmentException`.

* 🌐 **Modern Web UI**
  Interact with the Java backend through a modern glassmorphic HTML/CSS web interface without relying on bulky frameworks.

---

## 🛠️ Technologies Used

| Category          | Technology                          |
| ----------------- | ----------------------------------- |
| Backend           | Core Java                           |
| HTTP Server       | `com.sun.net.httpserver.HttpServer` |
| Frontend          | HTML5, CSS3, JavaScript             |
| API Communication | Fetch API                           |
| Architecture      | Object-Oriented Programming (OOP)   |
| Design            | Glassmorphism                       |
| IDE               | IntelliJ IDEA                       |

---

## 📂 Project Structure

```text
University_Enrollment_System/
├── .idea/
├── web/
│   └── index.html                    # HTML/CSS Frontend
├── src/
│   └── University_Enrollment_System/
│       ├── Main.java                 # Console application entry point
│       ├── UniversityWebServer.java  # Built-in Java HTTP Server
│       ├── Person.java               # Abstract base class
│       ├── Student.java              # Inherits Person
│       ├── Professor.java            # Inherits Person
│       ├── Course.java               # Manages enrollments
│       └── EnrollmentException.java  # Custom exception
├── LICENSE
└── README.md
```

---

## 🏛️ Architecture & OOP Mapping

### Class Architecture

* **Person (Abstract)**
  Acts as the base class and demonstrates abstraction for `Student` and `Professor`.

* **Student**
  Implements encapsulation and automatically generates unique `rollNo` values using static properties.

* **Professor**
  Represents the professor entity and can be assigned to courses.

* **Course**
  Acts as the core enrollment component. It demonstrates **Aggregation** by maintaining a list of enrolled `Student` objects and a `Professor`.

* **EnrollmentException**
  A custom exception extending Java's `Exception` class to handle enrollment capacity restrictions.

---

## 🌐 Server Architecture

The **UniversityWebServer** uses Java's native `HttpServer` to create and run the web application on port `8080`.

### API Endpoints

#### `POST /api/enroll`

Accepts URL-encoded form data submitted from the web interface, creates a `Student` object, and attempts to enroll the student into the course.

#### `GET /api/details`

Retrieves the current course details directly from the `Course` object.

---

## 🚀 How to Run the Project

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/University_Enrollment_System.git
```

### 2️⃣ Open the Project

Open the project in **IntelliJ IDEA** or your preferred Java IDE.

### 3️⃣ Compile the Source Files

Compile the Java source files using your IDE or Java compiler.

---

## 🌐 Option 1: Run the Web Application

The web interface is the recommended way to explore the project.

1. Open `UniversityWebServer.java`.
2. Run the application.
3. The server will start on port `8080`.
4. Open your browser.
5. Navigate to:

```text
http://localhost:8080
```

6. Use the web interface to test the university enrollment workflow.

---

## 📟 Option 2: Run the Console Application

Run:

```text
Main.java
```

The console application demonstrates:

* Student creation
* Professor creation
* Course creation
* Student enrollment
* Enrollment capacity handling
* Custom exception handling

---

## 🎯 OOP Concepts Demonstrated

This project provides practical implementation of several important Java OOP concepts:

```text
                 ┌─────────────────────┐
                 │   Person (Abstract)  │
                 └──────────┬──────────┘
                            │
                 ┌──────────┴──────────┐
                 ▼                     ▼
          ┌─────────────┐       ┌─────────────┐
          │   Student   │       │  Professor  │
          └──────┬──────┘       └──────┬──────┘
                 │                     │
                 └──────────┬──────────┘
                            ▼
                    ┌───────────────┐
                    │    Course     │
                    └───────┬───────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ EnrollmentException │
                 └─────────────────────┘
```

### Key Concepts

**🔹 Abstraction**
`Person` provides a common abstract structure for people within the university.

**🔹 Inheritance**
`Student` and `Professor` inherit common functionality from `Person`.

**🔹 Encapsulation**
Data is protected through appropriate class structures and controlled access.

**🔹 Aggregation**
`Course` maintains relationships with students and professors.

**🔹 Exception Handling**
`EnrollmentException` handles situations where course capacity is exceeded.

**🔹 Static Members**
Static properties are used for automatic student roll-number generation.

---

## 💡 Learning Outcomes

Through this project, the following practical concepts are demonstrated:

* Building applications using **Java OOP**
* Designing classes and relationships
* Implementing inheritance and abstraction
* Applying encapsulation and data hiding
* Working with custom exceptions
* Connecting a Java backend with a web interface
* Creating HTTP endpoints using Java's built-in server
* Using JavaScript Fetch API for backend communication
* Structuring a maintainable Java project

---

## 👨‍💻 Author

**Mahak Yadav**
*B.Tech — Artificial Intelligence & Data Science | IILM University*

* 🐙 **GitHub:** https://github.com/mahakyadav13-code
* 💼 **LinkedIn:** https://www.linkedin.com/in/mahak-yadav-59369a2a7/

---

## 📌 Note

This project was originally developed for **academic and learning purposes** to demonstrate Java Object-Oriented Programming concepts and university enrollment workflows.

The project has been enhanced with a custom **HTML/CSS web interface** to provide a more interactive way of testing and demonstrating the Java backend.

---

## ⭐ If You Find This Project Useful

If you found this project helpful for learning **Java OOP, backend development, or web integration**, consider giving the repository a ⭐ on GitHub.
