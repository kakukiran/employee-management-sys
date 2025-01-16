# Employee Management System

## Project Overview
The **Employee Management System** is a full-stack web application designed to manage employee records. It features a **ReactJS** frontend, **Spring Boot** backend, and a **MySQL** database. The application supports CRUD operations and demonstrates modern web development frameworks and tools.

## Technologies Used
- **Frontend**: ReactJS
- **Backend**: Spring Boot
- **Database**: MySQL
- **Tools**: Postman, Git/GitHub, Maven
- **IDEs**: Spring Tool Suite (STS), IntelliJ IDEA, Visual Studio Code

## Pre-requisites
Ensure the following software is installed on your system:
1. **Java JDK (version 8 or above)** and **Maven**.
2. **Node.js (version 16 or above)**.
3. **MySQL Server**.

### Development environments:
- **Spring Tool Suite (STS)** or **IntelliJ IDEA** for backend development.
- **Visual Studio Code** for frontend development.

## How to Execute the Project

### 1. Backend Setup (Spring Boot)
1. Launch your IDE (STS or IntelliJ IDEA) and set the workspace to `STS-workspace`.
2. Create a new Spring Starter Project with these dependencies:
   - **Spring Web**
   - **Spring Data JPA**
   - **MySQL Driver**
   - **Lombok**
   - **Spring Boot DevTools**
3. Configure the database in the `application.properties` file:
   ```properties
   server.port=9191
   spring.datasource.url=jdbc:mysql://localhost/employee_management_system
   spring.datasource.username=root
   spring.datasource.password=root
   spring.jpa.hibernate.ddl-auto=update
   spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect.
4. Use **MySQL commands** to create the schema and insert sample employee records:
   ```sql
   CREATE SCHEMA employee_management_system;

   USE employee_management_system;

   CREATE TABLE employees (
     id INT AUTO_INCREMENT PRIMARY KEY,
     first_name VARCHAR(10),
     last_name VARCHAR(10),
     email VARCHAR(50)
   );

   INSERT INTO employees (first_name, last_name, email) 
   VALUES 
        ('STEVE', 'JOBS', 'stevejobs@apple.com'),
        ('MARK', 'JUKERBERG', 'mark@meta.com'),
        ('ELON', 'MUSK', 'elonmusk@tesla.com'),
        ('JEFF', 'BEJOS', 'jeffbejos@amazon.com'),
        ('SUNDAR', 'PICHAI', 'sundarpichai@google.com');

   DESC employees;

   select * from employees;
5. Create packages for **model**, **repository**, **service**, and **controller** layers following MVC
principles.
6. Build the `model`, `repository`, `service`, and `controller` layers.:
   - **GET All Employees:** `/api/v1/employees`
   - **POST Add Employee:** `/api/v1/employees`
   - **PUT Update Employee by ID:** `/api/v1/employees/{id}`
   - **DELETE Remove Employee by ID:** `/api/v1/employees/{id}`
7. Run the Spring Boot application on `http://localhost:9191/`.
### 2 Frontend (ReactJS)
1. Open **VS Code** and set the workspace to `react-workspace`.
2. Create a React project:
   ```bash
   npx create-react-app react-frontend.
3. Install dependencies:
   ```bash
   npm install bootstrap axios react-router-dom
4. Structure the project as follows:
   ```plaintext
   src
   |--- components
   |   |--- EmployeeListComponent.js
   |   |--- CreateEmployeeComponent.js
   |   |--- UpdateEmployeeComponent.js
   |   |--- HeaderComponent.js
   |   |--- FooterComponent.js
   |
   |--- services
   |   |--- EmployeeService.js
5. Use `axios` to handle API requests and `react-router-dom` for routing.
6. Start the React development server:
   ```bash
   npm start
  The frontend should now open automatically in your default web 
  browser. If not, navigate to the URL displayed in the terminal.

## How to Run the Project

1. Start the **Spring Boot backend** using your IDE.
2. Start the **React frontend** by running `npm start` in the `react-frontend` folder.
3. Open the application in your browser at `http://localhost:3000/`.

## Features

   - **CRUD Operations:** Create, Read, Update, and Delete employee records.
   - **Responsive UI:** Styled using **Bootstrap**.
   - **API Integration:** The frontend consumes backend APIs for dynamic data interaction.
   - **Routing:** Seamless navigation with **React Router**.
## Folder Structure
   ```plaintext
    D:
    |--- Java Project
    | |--- STS-workspace (Backend code)
    | |--- react-workspace (Frontend code)
    | |--- Notes (Documentation and configurations)
