# Employee Management System (Spring Boot CRUD + REST API)

A simple **Spring Boot CRUD REST API** for managing employees. This project demonstrates:

* Building REST APIs with Spring Boot
* CRUD operations (Create, Read, Update, Delete)
* Layered architecture (Controller → Service → Repository)
* H2 database integration

---

## 🚀 Features

* Add new employee
* Get all employees
* Get employee by ID
* Update employee details
* Delete employee
* RESTful JSON responses

---

## 🛠️ Tech Stack

* **Java 17**
* **Spring Boot** (Web, JPA, DevTools)
* **HikariCP** (default connection pool)
* **H2/MySQL** database
* **Maven**

---

## 📁 Project Structure

```
src/main/java/com/example/employees
├── controller
│   └── EmployeeController.java
├── service
│   └── EmployeeService.java
├── repository
│   └── EmployeeRepository.java
├── model
│   └── Employee.java
└── exception
    └── ResourceNotFoundException.java
```

---

## ⚙️ Run Locally

### 1️⃣ Clone the project

```
git clone https://github.com/your-username/employee-crud-api.git
cd employee-crud-api
```

### 2️⃣ Build & Run

```
mvn spring-boot:run
```

Spring Boot will start on:

```
http://localhost:8080
```

---

## 🧪 API Endpoints

### ➤ **Create Employee**

`POST /api/employees`

```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "department": "IT"
}
```

### ➤ **Get All Employees**

`GET /api/employees`

### ➤ **Get Employee by ID**

`GET /api/employees/{id}`

### ➤ **Update Employee**

`PUT /api/employees/{id}`

### ➤ **Delete Employee**

`DELETE /api/employees/{id}`

---

## 🛢️ Database Configuration (H2)

Add this in `application.properties`:

```
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.jpa.hibernate.ddl-auto=update
spring.h2.console.enabled=true
```

H2 Console URL:

```
http://localhost:8080/h2-console
```

---


## 📜 License

This project is open-source and free to use.
