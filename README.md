# Employee Management System

A Java-based Employee Management System developed using **Spring Boot, Hibernate, Spring Data JPA, and MySQL**. This application provides RESTful APIs to manage employee and department information with CRUD operations, database relationships, validation, exception handling, and email notifications with attachments.

## Overview

The Employee Management System is a backend application designed to simplify employee and department management.

It follows a layered architecture that separates application responsibilities into Controller, Service, and Repository components, making the application easier to maintain and extend.

## Key Features

- **Employee Management:** Create, retrieve, update, and delete employee records.
- **Department Management:** Manage department information through REST APIs.
- **Entity Relationships:** Implemented One-to-Many relationships between departments and employees.
- **DTO Mapping:** Used DTOs and ModelMapper for converting between Entity and DTO objects.
- **Input Validation:** Implemented validation to maintain data accuracy.
- **Exception Handling:** Handles application-level exceptions.
- **Email Integration:** Sends email notifications with file attachments.
- **Database Integration:** Uses MySQL for persistent data storage.
- **Layered Architecture:** Separates Controller, Service, and Repository responsibilities.

## Technologies Used

| Category | Technologies |
|---|---|
| Programming Language | Java |
| Backend Framework | Spring Boot |
| ORM Framework | Hibernate |
| Persistence | Spring Data JPA |
| Database | MySQL |
| API Architecture | RESTful APIs |
| Object Mapping | ModelMapper, DTO |
| Build Tool | Maven |
| Email Integration | Spring Mail / SMTP |
| API Testing | Postman |
| Logging | SLF4J, Log4j |

## Project Architecture

The application follows a layered architecture:

```text
              Client / Postman
                     |
                     v
              REST Controller
                     |
                     v
                Service Layer
                     |
                     v
              Repository Layer
                     |
                     v
                  MySQL
```

**Layer Responsibilities:**

- **Controller Layer:** Handles incoming HTTP requests and returns API responses.
- **Service Layer:** Contains business logic and application processing.
- **Repository Layer:** Performs database operations using Spring Data JPA.
- **Entity Layer:** Represents database tables and relationships.
- **DTO Layer:** Transfers data between application layers.
- **Exception Handling:** Manages application exceptions and validation errors.

## Database Relationships

The application implements a **One-to-Many relationship** between Department and Employee entities.

- One department can have multiple employees.
- Each employee belongs to a department.
- Hibernate ORM and Spring Data JPA manage entity persistence and relationships.

## Prerequisites

Before running the application, ensure you have installed:

- Java JDK
- Spring Tool Suite (STS) or Eclipse IDE
- MySQL Server
- MySQL Workbench
- Maven
- Postman

## Installation and Setup

### 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### 2. Open the Project

Import the cloned project into Spring Tool Suite (STS) or Eclipse as an existing Maven project.

### 3. Configure MySQL

Create a MySQL database and update the database configuration in:

`src/main/resources/application.properties`

Configure the following properties with your local database details:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/YOUR_DATABASE_NAME
spring.datasource.username=YOUR_USERNAME
spring.datasource.password=YOUR_PASSWORD

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

Add your SMTP configuration separately if you want to use the email notification functionality.

**Note:** Never commit actual database passwords, email credentials, or other sensitive configuration details to GitHub.

### 4. Build the Project

Run the following Maven command:

```bash
mvn clean install
```

### 5. Run the Application

Run the Spring Boot application from your IDE or use:

```bash
mvn spring-boot:run
```

### 6. Test APIs

Open Postman and test the available Employee and Department REST endpoints.

## API Testing

The application exposes RESTful APIs for employee and department management.

Supported operations include:

- Create Employee
- Get Employee Details
- Update Employee
- Delete Employee
- Create Department
- Get Department Details
- Update Department
- Delete Department

Use Postman to send HTTP requests and verify API responses.

## Learning Outcomes

Through this project, I gained practical experience in:

- Developing RESTful APIs using Spring Boot.
- Implementing CRUD operations using Spring Data JPA.
- Managing entity relationships using Hibernate.
- Working with DTOs and ModelMapper.
- Implementing layered architecture.
- Handling exceptions and input validation.
- Integrating email notifications with attachments.
- Connecting Java applications with MySQL.

## Author

**Yogeshwar Kadam**

Java Developer | Spring Boot | Hibernate | Microservices

- LinkedIn: https://linkedin.com/in/yogeshwar-kadam-94b649258
- GitHub: https://github.com/YogeshwarKadam4393

---

⭐ If you find this project useful, consider giving it a star!
