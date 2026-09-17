# Loctech AWS Student Registration System

AWS EC2 + RDS Student Registration System — Loctech IT Training Institute Capstone Project

## Project Overview

This project is a Student Registration System deployed on Amazon Web Services (AWS).

The application allows student registration information to be submitted and provides CRUD functionality for managing student records.

The project was completed as part of the AWS Cloud Computing training at Loctech IT Training Institute.

## Project Objectives

The main objectives of this project are to:

- Build and deploy a web application on AWS.
- Create a secure AWS networking environment using a VPC.
- Host the application on an Ubuntu EC2 instance.
- Store student information in Amazon RDS MySQL.
- Connect the backend application to the database.
- Implement CRUD operations.
- Apply AWS security best practices.
- Monitor and manage the deployed application.

##  AWS Services and Technologies Used

- Amazon VPC — Network infrastructure
- Amazon EC2 — Application server
- Amazon RDS MySQL — Database
- Amazon Route 53 — DNS and domain routing
- Internet Gateway — Internet connectivity for the public subnet
- NAT Gateway — Outbound internet connectivity for private resources
- Security Groups — Network access control
- IAM — Identity and access management
- Amazon CloudWatch — Monitoring
- Apache — Web server
- Node.js — Backend runtime
- Express.js — Backend API
- MySQL — Relational database

## Application Architecture

The application follows this flow:

Student Browser
        ↓
Route 53
        ↓
EC2 / Apache
        ↓
Node.js Backend API
        ↓
Amazon RDS MySQL

Apache serves the frontend application and forwards API requests internally to the Node.js backend.

Node.js processes the requests and communicates with the RDS MySQL database.

## 🔹 Phase 1 — AWS Networking

The networking environment was created using Amazon VPC.

### Resources Created

- VPC
- Public Subnet
- Private Subnets
- Public Route Table
- Private Route Table
- Internet Gateway
- NAT Gateway
- Routes

The public subnet is used for the EC2 web server, while the database resources are kept in the private network.

## 🔹 Phase 2 — EC2

An Ubuntu EC2 instance was launched inside the project VPC.

### EC2 Configuration

- Ubuntu operating system
- EC2 Security Group
- SSH access
- Apache web server
- Node.js backend

The EC2 instance provides the compute environment where the web application and backend run.

## 🔹 Phase 3 — Amazon RDS MySQL

Amazon RDS was used as the managed database service.

A MySQL database was created to store student registration records.

### Database

Database name:

angeldb

Table:

students

The RDS database was configured without public access.

Database access is restricted through the RDS Security Group.

## 🔹 Phase 4 — Application and CRUD

The Student Registration System supports the main CRUD operations.

### CREATE

Register a new student.

### READ

Retrieve registered student information from the database.

### UPDATE

Modify existing student information.

### DELETE

Remove a student record from the database.

The backend API provides the connection between the frontend application and the RDS MySQL database.

## Application Testing

The deployed application was tested through the project domain.

Testing included:

- Opening the deployed website
- Registering student information
- Reading student records
- Updating student information
- Deleting student records
- Testing the EC2 to RDS connection
- Confirming the backend API was running

## Phase 5 — Security

Security controls were applied to protect the application and database.

### SSH

SSH access through port 22 was restricted to the administrator's permitted IP address.

### HTTPS

HTTPS was configured to provide secure communication between the browser and the web server.

### MySQL

MySQL port 3306 was not exposed to the public internet.

RDS accepts database traffic from the EC2 Security Group.

### Node.js

Node.js port 3000 is not publicly exposed.

Apache reverse-proxies API requests internally to the Node.js application.

### IAM

IAM was used to control AWS permissions according to the principle of least privilege.

##  Live Application

Project Website:

https://angelaws.online

## Frontend

The frontend was developed using:

- HTML
- CSS
- JavaScript

The frontend provides the student registration interface.

##  Backend

The backend was developed using:

- Node.js
- Express.js
- MySQL

The backend provides API endpoints for student registration and CRUD operations.

##  Database

Amazon RDS MySQL is used to store student registration information.

The main students table contains student information such as:

- Student ID
- Full Name
- Email Address
- Course

##  Data Flow

When a request is made through the application:

1. The user interacts with the frontend.
2. Apache receives the web request.
3. Apache forwards API requests to the Node.js backend.
4. Node.js processes the request.
5. Node.js communicates with Amazon RDS MySQL.
6. The database returns the requested result.
7. The result is returned to the frontend.

##  Project Screenshots

Screenshots documenting the AWS infrastructure, application deployment, database configuration, security configuration and application testing will be added to this repository.

##  Project Author

Angel Chibogwu Tabansi - Icheku

Loctech IT Training Institute

AWS Cloud Computing Training

## Project Summary

This project demonstrates how a web application can be deployed on AWS using EC2 for compute, RDS MySQL for data storage, VPC for networking, Security Groups for access control, IAM for permissions, and Apache and Node.js for application delivery.

The project follows the five major phases of the Loctech AWS capstone:

1. AWS Networking
2. EC2 and Application Deployment
3. RDS MySQL
4. Application, CRUD and Testing
5. Security Hardening
