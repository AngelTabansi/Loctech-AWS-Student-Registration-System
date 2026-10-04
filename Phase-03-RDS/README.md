# 🗄️ Phase 03 — Amazon RDS MySQL

## 📌 Overview

The third phase of the Loctech AWS Capstone Project focused on creating and configuring an Amazon RDS MySQL database for the Student Registration System.

Amazon RDS was used to provide a managed relational database for storing student registration information.

---

## 🎯 Objectives

The main objectives of this phase were to:

- Create an Amazon RDS MySQL database.
- Configure the database settings.
- Create a DB subnet group using private subnets.
- Configure the RDS Security Group.
- Create the application database.
- Create the database user.
- Connect the EC2 application to RDS.
- Store student information in MySQL.

---

## 🗄️ Amazon RDS MySQL

An Amazon RDS MySQL database was created for the project.

### Database Name

**Angel-Capstone-DB**

### Database Engine

**MySQL**

### Database

**angeldb**

RDS provides a managed database service, so the project does not need to manage the underlying database server manually.

---

## 🔐 Database Security

The RDS database was configured with:

**Public access: No**

This means the database cannot be accessed directly from the public internet.

The database is intended to communicate with the application running on the EC2 instance.

---

## 🌐 DB Subnet Group

A DB subnet group was created using private subnets in the VPC.

The database subnets were kept private because the database should not be directly accessible from the internet.

### Private Subnets

The RDS database uses private subnets created during Phase 1.

This provides an additional layer of network security.

---

## 🔒 RDS Security Group

A dedicated security configuration was used to control access to the RDS database.

### MySQL Port

**Port 3306**

Port 3306 was allowed only from the EC2 Security Group.

The database was not opened to:

**0.0.0.0/0**

This prevents direct public access to the MySQL database.

---

## 🔗 EC2 to RDS Connection

The Node.js backend running on the EC2 instance connects to the RDS MySQL database.

The application uses the RDS endpoint to communicate with the database.

The connection flow is:

**Browser → Apache → Node.js → RDS MySQL**

The browser does not connect directly to the database.

---

## 🗃️ Database Table

A `students` table was created in the `angeldb` database.

The table stores student registration information.

### Student Information

The table contains:

- Student ID
- Student Name
- Email Address
- Course

The student ID is automatically generated using an auto-incrementing primary key.

---

## 🔄 CRUD Operations

The Student Registration System implements CRUD operations.

### Create

Allows a new student record to be added to the database.

### Read

Retrieves registered student records from the database.

### Update

Allows existing student information to be updated.

### Delete

Allows a student record to be removed from the database.

---

## 🧪 Database Testing

The database connection was tested through the backend application.

Testing included:

- Connecting EC2 to RDS.
- Creating the students table.
- Adding student records.
- Retrieving student records.
- Updating student information.
- Deleting student records.
- Confirming communication between the backend and RDS.

---

## 🔑 Database Credentials

Database credentials were configured securely for the backend application.

Sensitive credentials were not included in the GitHub repository.

---

## 🛡️ Security Considerations

The following security practices were applied:

- RDS public access was disabled.
- MySQL port 3306 was not exposed to the internet.
- Access to RDS was restricted to the EC2 Security Group.
- The database was placed in private subnets.
- Database credentials were kept private.
- The application communicates with the database through the backend.

---

## 📸 Phase 3 Screenshots

Screenshots documenting the RDS configuration will be added to this folder.

### RDS Database

Amazon RDS database configuration.

### DB Subnet Group

Private subnet configuration for the RDS database.

### RDS Security Group

Security Group controlling MySQL access.

### Database Configuration

Database engine and configuration details.

### Database Connection

EC2 to RDS database connection.

### Students Table

The students table used by the application.

### CRUD Testing

Testing of Create, Read, Update and Delete operations.

---

## ✅ Phase 3 Completed

Amazon RDS MySQL was successfully configured as the database layer for the Student Registration System.

The database was placed in private subnets and protected using Security Group rules that allow MySQL access only from the EC2 application server.

The EC2 backend successfully communicates with RDS to store and manage student registration information.
