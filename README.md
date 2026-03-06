 # Banking Microservices System

## Overview

The **Banking Microservices System** is a scalable backend application built using **Java 17, Spring Boot 3, and Spring Cloud**. The project demonstrates how modern banking systems can be designed using a **microservices architecture**, where different functionalities are separated into independent services.

Each service runs independently and communicates with other services through **REST APIs and Feign Clients**, enabling better scalability, maintainability, and modular development.

The system includes services for **user authentication, account management, and transaction processing**, all managed through a centralized **API Gateway** with secure access using **JWT-based authentication**.

---

## Architecture

The system is composed of multiple independent microservices:

* **Eureka Server** – Service discovery for registering and locating microservices
* **API Gateway** – Central entry point for all client requests
* **User Service** – Handles user registration, authentication, and JWT token generation
* **Account Service** – Manages bank accounts and account details
* **Transaction Service** – Handles deposits, withdrawals, and transaction history

All services communicate using **REST APIs and Feign Clients**.

### Architecture Flow

Client → API Gateway → Eureka Service Discovery → Microservices

* User Service
* Account Service
* Transaction Service

The API Gateway routes incoming requests to the appropriate microservice while maintaining security and centralized access control.

---

## Key Features

* Microservices-based banking architecture
* Service discovery using **Netflix Eureka**
* Centralized request routing via **Spring Cloud Gateway**
* Secure authentication using **Spring Security and JWT**
* Inter-service communication using **Feign Clients**
* Independent service deployment and scalability
* RESTful APIs for banking operations

---

## Technologies Used

* **Java 17**
* **Spring Boot 3**
* **Spring Cloud 2024.x**
* **Spring Security**
* **JWT Authentication**
* **Spring Cloud Gateway**
* **Netflix Eureka Server**
* **Feign Client**
* **Maven**
* **REST APIs**
* **Postman**

---

## Microservices Included

### User Service

Handles authentication and user management.

Features:

* User registration
* Login authentication
* JWT token generation
* Secure endpoint access

---

### Account Service

Manages bank accounts and account-related operations.

Features:

* Account creation
* View account details
* Balance management

---

### Transaction Service

Handles financial transactions within the system.

Features:

* Deposit money
* Withdraw money
* Transaction history

---

### API Gateway

Acts as a centralized entry point for all external client requests.

Responsibilities:

* Request routing
* Security filtering
* Authentication validation

---

### Eureka Server

Provides **service discovery** for all microservices.

Responsibilities:

* Register services dynamically
* Enable service communication without hardcoding URLs

---

## Example API Endpoints

### User Authentication

POST /api/auth/login

Example Request

```
{
  "username": "user123",
  "password": "password"
}
```

---

### Create Account

POST /api/accounts/create

```
{
  "userId": 101,
  "accountType": "SAVINGS",
  "initialBalance": 5000
}
```

---

### Deposit Money

POST /api/transactions/deposit

```
{
  "accountId": 101,
  "amount": 2000
}
```

---

### Withdraw Money

POST /api/transactions/withdraw

```
{
  "accountId": 101,
  "amount": 1000
}
```

---

## Running the Project

Follow these steps to run the system locally.

Step 1: Start the **Eureka Server**

Step 2: Start the **User Service**

Step 3: Start the **Account Service**

Step 4: Start the **Transaction Service**

Step 5: Start the **API Gateway**

Step 6: Test APIs using **Postman**

All services will register automatically with **Eureka Server**, and requests will be routed through the **API Gateway**.

---

## Project Structure

```
banking-microservices-system
│
├── api-gateway
├── eureka-server
├── user-service
├── account-service
├── transaction-service
│
├── docs
│   └── architecture-diagram.png
│
├── postman
│   └── banking-api-collection.json
│
├── README.md
└── .gitignore
```

---

## Future Improvements

* Docker containerization for microservices
* Kubernetes deployment
* API rate limiting
* Distributed logging and monitoring
* Database per service architecture

---

## Author

**Bhaskar Chary**

Backend Developer | Java | Spring Boot | Microservices | AI/ML
