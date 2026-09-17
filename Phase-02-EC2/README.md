# 🖥️ Phase 02 — Amazon EC2

## 📌 Overview

The second phase of the Loctech AWS Capstone Project focused on launching and configuring an Amazon EC2 instance to host the Student Registration System.

An Ubuntu EC2 instance was deployed inside the VPC created during Phase 1.

---

## 🎯 Objectives

The main objectives of this phase were to:

- Launch an Ubuntu EC2 instance.
- Configure the EC2 Security Group.
- Connect to the server using SSH.
- Install and configure the web server.
- Install Node.js for the backend application.
- Deploy the Student Registration System.
- Assign a stable public address to the server.
- Configure the application for web access.

---

## 🖥️ EC2 Instance

### Instance Name

**Angel-Capstone-Web-Server**

The EC2 instance provides the compute environment for the Student Registration System.

It runs the web server and Node.js backend application.

### Operating System

**Ubuntu**

Ubuntu was selected as the operating system for the application server.

---

## 🔐 EC2 Security Group

A dedicated Security Group was created for the EC2 instance.

The Security Group controls the network traffic allowed to reach the server.

### Allowed Traffic

- **HTTP — Port 80** — Web traffic
- **HTTPS — Port 443** — Secure web traffic
- **SSH — Port 22** — Administrative access from the permitted administrator IP address

The Node.js application runs internally on port 3000 and is not exposed directly to the public internet.

---

## 🔑 SSH Connection

PowerShell was used to connect securely to the Ubuntu EC2 instance using SSH.

SSH provided secure command-line access to the Linux EC2 server, allowing server administration and application deployment.

The private SSH key was kept securely and was not uploaded to the GitHub repository.
---

## 🌐 Apache Web Server

Apache was installed and configured on the EC2 instance.

Apache is responsible for serving the frontend application to visitors.

It also acts as a reverse proxy for the Node.js backend API.

### Simple Explanation

**Apache serves my website and forwards API requests to my Node.js backend.**

---

## ⚙️ Node.js Backend

Node.js was installed on the EC2 instance to run the backend application.

The backend processes requests from the frontend and communicates with Amazon RDS MySQL.

The application uses Express.js to provide the backend API.

### Backend Responsibilities

- Receive registration requests.
- Process student information.
- Communicate with the database.
- Perform CRUD operations.
- Return results to the frontend.

---

## 🔄 PM2 Process Manager

PM2 was used to manage the Node.js backend application.

PM2 keeps the backend application running and allows it to restart automatically when required.

The backend application was configured to start automatically after server restart.

---

## 🌍 Elastic IP

An Elastic IP was associated with the EC2 instance.

An Elastic IP provides a stable public IPv4 address for the server.

This makes it possible to consistently access the deployed application and connect the domain name to the EC2 server.

---

## 🌐 Domain Name

The project domain was configured to point to the EC2 server.

### Project Domain

**angelaws.online**

Amazon Route 53 was used for DNS configuration.

The domain points to the EC2 Elastic IP address.

---

## 🔒 HTTPS

HTTPS was configured for the project domain.

A valid SSL/TLS certificate was installed using Certbot and Let's Encrypt.

This allows visitors to securely access the application using:

**https://angelaws.online**

---

## 🚀 Application Deployment

The Student Registration System frontend was deployed to the Apache web server.

The backend Node.js application runs on the EC2 instance and communicates with the Amazon RDS MySQL database.

The overall application flow is:

**Browser → Apache → Node.js → RDS MySQL**

---

## 🔄 Apache Reverse Proxy

Apache was configured to forward API requests internally to the Node.js backend.

The browser accesses the API through the website domain rather than directly accessing port 3000.

This improves the security of the application because the Node.js port does not need to be publicly exposed.

---

## 🧪 Testing

The EC2 deployment was tested by:

- Connecting to the server through SSH.
- Confirming Apache was running.
- Confirming the Node.js backend was running.
- Testing the application through the domain.
- Testing communication between the backend and RDS.
- Testing student registration and CRUD operations.
- Confirming HTTPS access.

---

## 📸 Phase 2 Screenshots

Screenshots documenting the EC2 deployment and configuration will be added below.

### EC2 Instance

EC2 instance configuration and details.

### Security Group

EC2 Security Group and allowed traffic.

### SSH

Secure connection to the Ubuntu EC2 server.

### Apache

Apache web server configuration.

### Node.js

Node.js backend deployment.

### PM2

PM2 process management.

### Elastic IP

Elastic IP associated with the EC2 instance.

### Domain and HTTPS

Domain configuration and secure HTTPS access.

---

## ✅ Phase 2 Completed

The Ubuntu EC2 instance was successfully launched and configured to host the Student Registration System.

The frontend was deployed using Apache, while the Node.js backend runs on the EC2 server and communicates with Amazon RDS MySQL.

The server was secured by controlling inbound traffic through the EC2 Security Group.
