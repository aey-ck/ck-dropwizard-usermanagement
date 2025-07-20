**EmployeeManagement**

A sample Dropwizard project for managing employee data with CRUD operations, built using Java and MongoDB.Project URL: https://github.com/aey-ck/ck-dropwizard-usermanagement

**Overview**

This project provides a RESTful API for performing Create, Read, Update, and Delete (CRUD) operations on employee records. It is built using the Dropwizard framework for creating production-ready RESTful web services and MongoDB as the NoSQL database for storing employee data.

**Features**

Create: Add new employee records.
Read: Retrieve employee details by ID or fetch all employees.
Update: Modify existing employee records.
Delete: Remove employee records from the database.

RESTful API endpoints for seamless integration.
MongoDB integration for persistent storage.

**Technologies Used
**

Java: Core programming language.
Dropwizard: Framework for building RESTful services.
MongoDB: NoSQL database for storing employee data.
Maven: Build tool for dependency management and project setup.

**Prerequisites**

To run this project, ensure you have the following installed:

Java 17 or higher
MongoDB (local or cloud instance)
Maven 3.6 or higher
Git (optional, for cloning the repository)

**Setup Instructions
**

**Clone the Repository
**
git clone https://github.com/aey-ck/ck-dropwizard-usermanagement.git
cd ck-dropwizard-usermanagement


**Configure MongoDB
**
Ensure MongoDB is running locally or provide a connection string to a cloud instance.
Update the MongoDB configuration in config.yml with your database details:database:
  uri: mongodb://localhost:27017/employee_db




Build the Project
mvn clean install


Run the Application
java -jar target/EmployeeManagement-1.0-SNAPSHOT.jar server config.yml

