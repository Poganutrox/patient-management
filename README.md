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
