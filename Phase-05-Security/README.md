# 🔐 Phase 05 — Security Hardening

## 📌 Overview

The fifth phase of the Loctech AWS Capstone Project focused on securing the Student Registration System deployed on Amazon Web Services (AWS).

Security measures were implemented to restrict administrative access, protect the database, and control communication between AWS resources.

## 🎯 Objectives

- Restrict SSH access to the EC2 instance.
- Prevent public access to the MySQL database port.
- Allow database connections only from the EC2 Security Group.
- Apply appropriate IAM permissions.
- Improve the security of the deployed application.

## 🛡️ Security Measures Implemented

### 1. SSH Access Restriction

SSH access to the EC2 instance is restricted to the administrator's current public IP address.

**Purpose:** To reduce unauthorized access to the Linux server.

### 2. Database Protection

The Amazon RDS MySQL database is not publicly accessible.

Port 3306 is not open to the internet. Database traffic is permitted only from the EC2 Security Group.

**Purpose:** To protect student registration data from direct public access.

### 3. Security Groups

The EC2 Security Group controls access to the web server.

- HTTP — Port 80
- HTTPS — Port 443
- SSH — Port 22, restricted to the administrator's IP address

The Node.js backend uses port 3000 internally and is not exposed through a public inbound security-group rule.

### 4. IAM Permissions

An IAM role is attached to the EC2 instance for the required CloudWatch monitoring permissions.

**Purpose:** To allow AWS resources to access authorized services without unnecessarily granting broad permissions.

## ✅ Security Outcome

The security configuration reduces unnecessary public access and restricts database connectivity to the application server.

## 🏁 Conclusion

Phase 5 completes the security-hardening stage of the Loctech AWS Student Registration System capstone project.
