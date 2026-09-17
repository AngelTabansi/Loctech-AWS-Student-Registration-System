# 🚀 Phase 01 — AWS Networking

## 📌 Overview

The first phase of the Loctech AWS Capstone Project focused on building the network infrastructure required to host the Student Registration System securely.

Amazon VPC was used to create an isolated network environment for the project.

---

## 🎯 Objectives

The main objectives of this phase were to:

- Create a dedicated VPC for the capstone project.
- Create public and private subnets.
- Configure route tables.
- Create and attach an Internet Gateway.
- Configure a NAT Gateway for outbound internet connectivity.
- Prepare the network for EC2 and RDS.

---

## 🌐 VPC

### VPC Name

**Angel-Capstone-VPC**

### CIDR Block

**10.0.0.0/16**

The VPC provides the main private network environment for the AWS resources used in this project.

---

## 📦 Subnets

### 🟢 Public Subnet

**Angel-Capstone-Public-Subnet**

CIDR:

**10.0.1.0/24**

Availability Zone:

**eu-north-1a**

The public subnet is used for resources that need internet access, including the EC2 web server.

### 🔵 Private Subnets

Private subnets were created for resources that should not be directly accessible from the public internet.

The private network is used to support the database layer and improve the security of the application architecture.

---

## 🛣️ Route Tables

Route tables were configured to control how network traffic moves within the VPC.

### Public Route Table

The public route table directs internet-bound traffic through the Internet Gateway.

### Private Route Table

The private route table provides controlled outbound connectivity through the NAT Gateway.

---

## 🌍 Internet Gateway

An Internet Gateway was created and attached to the VPC.

It provides communication between the VPC's public subnet and the internet.

The Internet Gateway allows the public-facing EC2 server to receive web traffic.

---

## 🔄 NAT Gateway

A NAT Gateway was configured to provide outbound internet connectivity for resources in private subnets.

### Simple Explanation

A NAT Gateway allows private resources to access the internet for necessary outbound connections without making those resources directly accessible from the internet.

---

## 🔐 Network Security

The network was designed so that public-facing resources and private resources have different levels of internet exposure.

The database layer is kept private and is not directly exposed to the public internet.

---

## 🏗️ Phase 1 Architecture

**Internet**

⬇️

**Internet Gateway**

⬇️

**Public Subnet**

⬇️

**EC2 Web Server**

⬇️

**Private Network**

⬇️

**RDS MySQL Database**

---

## 📸 Phase 1 Screenshots

Screenshots documenting the networking configuration will be added below.

### VPC

AWS VPC configuration screenshot.

### Subnets

Public and private subnet configuration screenshots.

### Route Tables

Route table configuration screenshots.

### Internet Gateway

Internet Gateway configuration screenshot.

### NAT Gateway

NAT Gateway configuration screenshot.

---

## ✅ Phase 1 Completed

The AWS networking foundation was successfully created and prepared for the EC2 application server and RDS MySQL database.

### Key Services

- ☁️ Amazon VPC
- 🌐 Internet Gateway
- 🔄 NAT Gateway
- 📦 Public Subnet
- 🔒 Private Subnets
- 🛣️ Route Tables
