# 🏥 Patient Management System

A microservices-based RESTful API built with **Spring Boot**, designed for managing patients in a clinical environment. It handles CRUD operations, user authentication, and service-to-service communication, with a focus on clean architecture and scalability.

## 🔧 Tech Stack

- **Java 21**
- **Spring Boot 3**
- **Spring Cloud Config**
- **Spring Data JPA**
- **Spring Security + JWT**
- **Spring Gateway**
- **PostgreSQL**
- **Docker**
- **OpenAPI / Swagger UI**

## 🧱 Architecture Overview

This project follows a **microservices architecture**, with communication between services done using multiple protocols for efficiency and scalability:

- **HTTP REST** via Spring Cloud Gateway for client-to-service communication.
- **gRPC** for internal communication between microservices (e.g., Patient → Billing Service).
- **Apache Kafka** for asynchronous, event-driven communication (e.g., Patient → Analytics Service).

### 🔄 Communication Flow

- The **Frontend** makes HTTP requests through the **API Gateway** (`localhost:4000`) which routes to internal services.
- The **Patient Service** sends asynchronous events to **Analytics Service** via **Kafka**.
- It also communicates synchronously with the **Billing Service** using **gRPC** with Protocol Buffers.

### 📖 Microservices summary

The system is composed of several independent microservices:

- **api-gateway**: Routes requests to the appropriate microservices.
- **auth-service**: Handles authentication and issues JWT tokens.
- **patient-service**: Manages patient records (CRUD).
- **user-service**: Manages system users.
- **billing-service**: Handles billing and payment-related operations.
- **analytics-service**: Collects and provides statistical health data.
- **integration-tests**: Contains integration tests for the full system.

## 🚀 How to Run the Project

1. Clone the repository:

   ```bash
   git clone https://github.com/Poganutrox/patient-management.git
   cd patient-management
2. Launch all containers:

   ```bash
   docker-compose up --build
