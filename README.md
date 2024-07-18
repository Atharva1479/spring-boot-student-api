# Spring Boot Student API

This is a simple CRUD (Create, Read, Update, Delete) API built using Spring Boot. The API allows you to manage a database of students, including their details such as name, age, course, and email. This project demonstrates the basics of building RESTful web services with Spring Boot and includes functionalities to interact with a MySQL database.

## Features

- **Create a new student**: Add a new student to the database.
- **Retrieve all students**: Get a list of all students.
- **Retrieve a student by ID**: Fetch the details of a specific student by their ID.
- **Update a student**: Modify the details of an existing student.
- **Delete a student**: Remove a student from the database.

## Endpoints

| HTTP Method | Endpoint                | Description                    |
|-------------|-------------------------|--------------------------------|
| POST        | `/api/students`         | Create a new student           |
| GET         | `/api/students`         | Retrieve all students          |
| GET         | `/api/students/{id}`    | Retrieve a student by ID       |
| PUT         | `/api/students/{id}`    | Update a student's details     |
| DELETE      | `/api/students/{id}`    | Delete a student               |

## Setup and Installation

### Prerequisites

- Java 8 or higher
- Maven
- MySQL

### Steps to Setup

1. **Clone the repository**

    ```bash
    git clone https://github.com/Atharva1479/spring-boot-student-api.git
    cd spring-boot-student-api
    ```

2. **Configure MySQL Database**

    Create a MySQL database named `studentdb` and update the `application.properties` file with your database username and password.

    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/studentdb
    spring.datasource.username=your-username
    spring.datasource.password=your-password
    spring.jpa.hibernate.ddl-auto=update
    ```

3. **Build and run the app using Maven**

    ```bash
    mvn spring-boot:run
    ```

    The app will start running at <http://localhost:8080>.

## Testing the API

You can use tools like `curl` or Postman to test the API endpoints. Refer to the [API documentation](#endpoints) for the available endpoints and their details.

### Example Requests using `curl`

- **Create a new student**

    ```bash
    curl -X POST http://localhost:8080/api/students -H "Content-Type: application/json" -d "{\"name\": \"John Doe\", \"age\": 20, \"course\": \"Computer Science\", \"email\": \"john.doe@example.com\"}"
    ```

- **Get all students**

    ```bash
    curl -X GET http://localhost:8080/api/students
    ```

- **Get a student by ID**

    ```bash
    curl -X GET http://localhost:8080/api/students/1
    ```

- **Update a student**

    ```bash
    curl -X PUT http://localhost:8080/api/students/1 -H "Content-Type: application/json" -d "{\"name\": \"John Smith\", \"age\": 21, \"course\": \"Mathematics\", \"email\": \"john.smith@example.com\"}"
    ```

- **Delete a student**

    ```bash
    curl -X DELETE http://localhost:8080/api/students/1
    ```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

