# Task Manager API

[![Build](https://img.shields.io/badge/build-passing-brightgreen.svg)](#)
[![Java](https://img.shields.io/badge/Java-17-blue.svg)](#)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-green.svg)](#)
[![License](https://img.shields.io/badge/license-MIT-lightgrey.svg)](LICENSE)

The **Task Manager API** is a backend RESTful service for managing personal tasks.  
It supports user authentication, task CRUD operations, and API documentation.  
This project is developed as part of **Semester 4 coursework** and serves as a **portfolio project** for applying as a Fresher Java Backend Developer.

---

## 🚀 Features (MVP v0.1.0)

- ✅ User Registration & Login with JWT Authentication
- ✅ Task Management (Create / Read / Update / Delete)
- 🔄 API Documentation with Swagger UI *(planned)*
- 🔄 Centralized Error Handling *(planned)*
- 🔄 Continuous Integration with GitHub Actions *(planned)*

---

## 🧰 Tech Stack

- **Language**: Java 17
- **Framework**: Spring Boot 3
- **Database**: PostgreSQL + Flyway Migration
- **ORM**: Spring Data JPA
- **Security**: Spring Security + JWT
- **Testing**: JUnit 5, Testcontainers
- **Documentation**: Swagger / OpenAPI
- **DevOps**: Docker, GitHub Actions CI

---

## 📐 UML Diagrams

- **Use Case** → [`docs/uml/usecase-student-management.drawio`](docs/uml/usecase-student-management.drawio)
- **ERD** → *(to be added)*
- **Class Diagram** → *(to be added)*

> Example (exported as PNG):
> ```markdown
> ![Use Case](docs/uml/usecase-student-management.png)
> ```
---

## 🗂 Project Structure
```
task-manager-api/
├─ docs/
│ └─ uml/ # UML diagrams (Use Case, ERD, Class, Sequence)
├─ src/
│ ├─ main/
│ │ ├─ java/com/lqhuy/taskmanager/ # Main application source
│ │ └─ resources/
│ │ ├─ application.yml # Application configuration
│ │ └─ db/migration/ # Flyway migration scripts (V1__init.sql, etc.)
│ └─ test/
│ └─ java/com/lqhuy/taskmanager/ # Unit & Integration tests
├─ .gitignore
├─ pom.xml
└─ README.md
```

---

## 🏗 How to Run

### Prerequisites
- Java 17+
- Maven 3.9+
- PostgreSQL 14+ (or Docker)

### Configure `application.yml`
```yaml
spring:
  datasource:
    url: jdbc:postgresql://localhost:5432/task_manager
    username: postgres
    password: your_password
  jpa:
    hibernate:
      ddl-auto: validate
  flyway:
    enabled: true
server:
  port: 8080
```
### Run the Application
```
mvn spring-boot:run
# or
mvn clean package
java -jar target/*.jar
```
### Access Swagger (after implementation)
```
http://localhost:8080/swagger-ui/index.html
```
---
## 🧪 Testing 
Run unit and integration tests:
```
mvn test
```
---
## 📅 Roadmap
- **Sprint 0**: Bootstrap Spring Boot, Flyway, Swagger, CI build
- **Sprint 1**: Authentication (Register/Login with JWT)
- **Sprint 2**: Task CRUD, Validation, Global Exception Handler
- **Sprint 3**: Integration Tests (Testcontainers), Docker Compose setup
---
## 👤 Author
**Le Quang Huy**
- **GitHub**: @lqhuy03
- **Email**: quanghuy.le.dev@gmail.com
- **LinkedIn**: [linkedin.com/in/le-quang-huy-322ab5379](https://www.linkedin.com/in/le-quang-huy-322ab5379/)
---
## License
This project is licensed under the [MIT License](LICENSE).
