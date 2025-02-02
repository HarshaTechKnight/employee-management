Employee Management System

![Java](https://img.shields.io/badge/Java-17-blue)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-2.7.x-green)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-13-blue)
![REST API](https://img.shields.io/badge/REST%20API-Yes-brightgreen)

The Employee Management System is a web-based application built using Java, Spring Boot, and PostgreSQL. It provides RESTful APIs to manage employee data, including creating, reading, updating, and deleting employee records.

---

Features

- Create Employee: Add a new employee to the system.
- Get Employee: Retrieve employee details by ID.
- Get All Employees: Fetch a list of all employees.
- Update Employee: Modify existing employee details.
- Delete Employee: Remove an employee from the system.

---

Technologies Used

- Java 17: The core programming language.
- Spring Boot: Framework for building the application.
- Spring Data JPA: For database operations.
- PostgreSQL: Relational database for storing employee data.
- REST API: Exposes endpoints for CRUD operations.
- Maven: Build and dependency management tool.

---

Prerequisites

Before running the application, ensure you have the following installed:

1. Java Development Kit (JDK) 17 or higher.
2. PostgreSQL installed and running.
3. Maven for building the project.
4. Postman or any API testing tool (optional).

---

Setup and Installation

1. Clone the Repository

```bash
git clone https://github.com/your-username/employee-management-system.git
cd employee-management-system
```

2. Configure PostgreSQL

1. Create a database named `employee_management` in PostgreSQL.
2. Update the `application.properties` file with your PostgreSQL credentials:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/employee_management
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect
```

3. Build and Run the Application

```bash
mvn clean install
mvn spring-boot:run
```

The application will start on `http://localhost:8080`.

---

API Endpoints

| HTTP Method | Endpoint                | Description                          |
|-------------|-------------------------|--------------------------------------|
| `GET`       | `/api/employees`        | Get all employees.                   |
| `GET`       | `/api/employees/{id}`   | Get an employee by ID.               |
| `POST`      | `/api/employees`        | Create a new employee.               |
| `PUT`       | `/api/employees/{id}`   | Update an existing employee.         |
| `DELETE`    | `/api/employees/{id}`   | Delete an employee.                  |

---

Example Requests

Create an Employee
```http
POST /api/employees
Content-Type: application/json

{
  "firstName": "John",
  "lastName": "Doe",
  "email": "john.doe@example.com"
}
```

Get All Employees
```http
GET /api/employees
```

Get Employee by ID
```http
GET /api/employees/1
```

Update an Employee
```http
PUT /api/employees/1
Content-Type: application/json

{
  "firstName": "Jane",
  "lastName": "Doe",
  "email": "jane.doe@example.com"
}
```

Delete an Employee
```http
DELETE /api/employees/1
```

---

Database Schema

The `employee` table has the following structure:

| Column Name | Data Type      | Description                |
|-------------|----------------|----------------------------|
| `id`        | BIGINT (PK)    | Unique identifier.         |
| `first_name`| VARCHAR(255)   | Employee's first name.     |
| `last_name` | VARCHAR(255)   | Employee's last name.      |
| `email`     | VARCHAR(255)   | Employee's email address.  |

---

Contributing

Contributions are welcome! If you'd like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeatureName`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeatureName`).
5. Open a pull request.

---

License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Acknowledgments

- Built with ❤️ using Spring Boot and PostgreSQL.
- Inspired by real-world employee management systems.

---

Contact

For any questions or feedback, please reach out:

- Your Name  
- Email: sriharsha0413@gmail.com  
- GitHub: [HarshaTechKnight](https://github.com/HarshaTechKnight)

---

Enjoy using the Employee Management System! 🚀
