# 🚀 Employee Management Microservices System

![Java](https://img.shields.io/badge/Java-17-orange)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.x-green)
![Spring Cloud](https://img.shields.io/badge/Spring_Cloud-2023.x-blue)
![Microservices](https://img.shields.io/badge/Architecture-Microservices-success)
![Database](https://img.shields.io/badge/Database-MySQL-blue)
![License](https://img.shields.io/badge/License-MIT-green)

A **Microservices-based Employee Management System** built using **Spring Boot**, **Spring Cloud**, **Eureka Server**, **Spring Cloud Gateway**, **Config Server**, **Spring Security**, and **MySQL**.

This project demonstrates how independently deployable microservices communicate through **REST APIs**, perform **Service Discovery**, and expose a single entry point through an **API Gateway**.

---

# 📑 Table of Contents

- Overview
- Features
- Tech Stack
- System Architecture
- Project Flow
- Microservices
- Folder Structure
- Database Design
- REST APIs
- Installation
- Running the Project
- Service Startup Order
- Key Learnings
- Future Enhancements
- Author

---

# 📌 Overview

This project demonstrates a production-style **Spring Boot Microservices Architecture** where multiple independent services communicate through REST APIs.

The application includes:

- Authentication Service
- Employee Service
- Address Service
- API Gateway
- Eureka Server
- Config Server

Each service follows the **Single Responsibility Principle** and can be deployed independently.

---

# ✨ Features

## Authentication Service

- User Registration
- User Login
- JWT Authentication
- Protected REST APIs

---

## Employee Service

- Employee CRUD Operations
- Employee Information Management
- REST APIs

---

## Address Service

- Address CRUD Operations
- Employee Address Management

---

## Spring Cloud Components

- Eureka Service Discovery
- API Gateway Routing
- Centralized Configuration
- Inter-service Communication
- Independent Deployment

---

# 🛠 Tech Stack

| Category | Technologies |
|-----------|--------------|
| Language | Java 17 |
| Framework | Spring Boot |
| Cloud | Spring Cloud |
| Service Discovery | Eureka Server |
| API Gateway | Spring Cloud Gateway |
| Configuration | Config Server |
| Security | Spring Security |
| Database | MySQL |
| ORM | Spring Data JPA |
| Build Tool | Maven |
| Testing | Postman |

---

# 🏗 System Architecture

```text
                     Client

                        │

                        ▼

             Spring Cloud Gateway

                        │

                        ▼

                 Eureka Server

                        │

     ┌──────────────────┼──────────────────┐

     ▼                  ▼                  ▼

Authentication     Employee Service   Address Service

     │                  │                  │

     └──────────────────┼──────────────────┘

                        ▼

                     MySQL
```

---

# 🔄 Project Flow

```text
Client Request

      │

      ▼

API Gateway

      │

      ▼

Eureka Server

      │

      ▼

Locate Required Service

      │

      ▼

Authentication Service
Employee Service
Address Service

      │

      ▼

Business Logic

      │

      ▼

Spring Data JPA

      │

      ▼

MySQL Database

      │

      ▼

JSON Response
```

---

# 📦 Microservices

## API Gateway

- Single Entry Point
- Request Routing
- Load Balancing
- Route Configuration

---

## Eureka Server

- Service Registration
- Service Discovery
- Health Monitoring

---

## Config Server

- Centralized Configuration
- Externalized Properties
- Environment-specific Configurations

---

## Authentication Service

- User Login
- User Registration
- JWT Authentication
- Authorization

---

## Employee Service

- Employee CRUD
- Employee Details
- Employee Search

---

## Address Service

- Address CRUD
- Employee Address Mapping

---

# 📂 Folder Structure

```text
Microservices-Project

├── api-gateway
├── eureka-server
├── config-server
├── authentication-service
├── employee-service
├── address-service
└── common-library
```

---

# 🗄 Database Design

## Authentication Database

```text
User

--------------------

id
username
password
role
```

---

## Employee Database

```text
Employee

--------------------

id
name
email
department
addressId
```

---

## Address Database

```text
Address

--------------------

id
city
state
country
zipcode
```

---

# 🔗 REST APIs

## Authentication

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | /auth/register | Register User |
| POST | /auth/login | Login User |

---

## Employee

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | /employees | Get All Employees |
| GET | /employees/{id} | Get Employee |
| POST | /employees | Create Employee |
| PUT | /employees/{id} | Update Employee |
| DELETE | /employees/{id} | Delete Employee |

---

## Address

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | /address/{id} | Get Address |
| POST | /address | Add Address |
| PUT | /address/{id} | Update Address |
| DELETE | /address/{id} | Delete Address |

---

---

# ⚙ Installation

```bash
git clone https://github.com/LUVKUMAR01/Microservices-Project.git

cd Microservices-Project
```

---

# ▶ Running the Project

Start services in the following order:

1. Config Server
2. Eureka Server
3. API Gateway
4. Authentication Service
5. Address Service
6. Employee Service

---

# 📊 Service Communication

```text
Client

↓

API Gateway

↓

Eureka Server

↓

Employee Service

↓

Address Service

↓

Database

↓

JSON Response
```

---

# 🔐 Security

- Spring Security
- JWT Authentication
- Stateless Authentication
- Protected REST APIs

---

# 📚 Key Learnings

- Spring Boot Microservices
- Service Discovery using Eureka
- API Gateway Routing
- Config Server
- REST API Design
- Spring Data JPA
- Inter-service Communication
- Distributed System Architecture

---

# 🚀 Future Enhancements

- Docker Containerization
- Docker Compose
- Kubernetes Deployment
- OpenFeign Client
- Resilience4j Circuit Breaker
- Kafka Event Streaming
- Redis Caching
- Prometheus Monitoring
- Grafana Dashboard
- CI/CD with Jenkins
- AWS Deployment

---

# 👨‍💻 Author

**Luv Kumar**

Java Backend Developer

GitHub: https://github.com/LUVKUMAR01

LinkedIn: *(Add your LinkedIn Profile)*

---

# ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub.
