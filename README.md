EmployeeManagement
A sample Dropwizard project for managing employee data with CRUD operations, built using Java and MongoDB.Project URL: https://github.com/aey-ck/ck-dropwizard-usermanagement
Overview
This project provides a RESTful API for performing Create, Read, Update, and Delete (CRUD) operations on employee records. It is built using the Dropwizard framework for creating production-ready RESTful web services and MongoDB as the NoSQL database for storing employee data.
Features

Create: Add new employee records.
Read: Retrieve employee details by ID or fetch all employees.
Update: Modify existing employee records.
Delete: Remove employee records from the database.
RESTful API endpoints for seamless integration.
MongoDB integration for persistent storage.

Technologies Used

Java: Core programming language.
Dropwizard: Framework for building RESTful services.
MongoDB: NoSQL database for storing employee data.
Maven: Build tool for dependency management and project setup.

Prerequisites
To run this project, ensure you have the following installed:

Java 17 or higher
MongoDB (local or cloud instance)
Maven 3.6 or higher
Git (optional, for cloning the repository)

Setup Instructions

Clone the Repository
git clone https://github.com/aey-ck/ck-dropwizard-usermanagement.git
cd ck-dropwizard-usermanagement


Configure MongoDB

Ensure MongoDB is running locally or provide a connection string to a cloud instance.
Update the MongoDB configuration in config.yml with your database details:database:
  uri: mongodb://localhost:27017/employee_db




Build the Project
mvn clean install


Run the Application
java -jar target/EmployeeManagement-1.0-SNAPSHOT.jar server config.yml


Access the APIThe application will start on http://localhost:8080. Use tools like Postman or curl to interact with the API.


API Endpoints



Method
Endpoint
Description



GET
/employees
Retrieve all employees


GET
/employees/{id}
Retrieve an employee by ID


POST
/employees
Create a new employee


PUT
/employees/{id}
Update an existing employee


DELETE
/employees/{id}
Delete an employee by ID


Example Request (Create Employee)
curl -X POST http://localhost:8080/employees \
-H "Content-Type: application/json" \
-d '{"name":"John Doe","email":"john.doe@example.com","department":"Engineering"}'

Example Response
{
  "id": "507f1f77bcf86cd799439011",
  "name": "John Doe",
  "email": "john.doe@example.com",
  "department": "Engineering"
}

Project Structure
ck-dropwizard-usermanagement/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   ├── com.example.employeemanagement/
│   │   │   │   ├── model/         # Employee data model
│   │   │   │   ├── resource/      # RESTful API endpoints
│   │   │   │   ├── service/       # Business logic
│   │   │   │   ├── config/        # Dropwizard configuration
│   │   │   │   └── Application.java # Main application class
│   │   └── resources/
│   │       └── config.yml         # Configuration file
├── pom.xml                        # Maven dependencies
└── README.md                      # This file

Running Tests
To run the unit tests:
mvn test

Contributing
Contributions are welcome! Please follow these steps:

Fork the repository.
Create a new branch (git checkout -b feature-branch).
Make your changes and commit (git commit -m "Add feature").
Push to the branch (git push origin feature-branch).
Create a pull request.

License
This project is licensed under the MIT License. See the LICENSE file for details.
Contact
For any questions or issues, please open an issue on GitHub or contact Akhil CK via LinkedIn.
