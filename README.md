# 📚 Bookstore E-Commerce Microservices

### Production-Ready Monorepo Architecture

**Spring Boot 3.x + Spring Cloud | Java 17+**

---

## 🚀 Overview

This project is a **scalable, production-ready backend system** for a bookstore e-commerce platform, built using a **microservices architecture**.

It replaces a traditional monolithic backend with **independent, loosely coupled services**, enabling better scalability, maintainability, and deployment flexibility.

---

## 🏗️ System Architecture

The application is decomposed into multiple microservices, where each service:

* Owns its own database (**Database-per-Service pattern**)
* Exposes RESTful APIs
* Communicates via:

  * HTTP (synchronous)
  * Kafka (asynchronous)
* Is routed through a centralized **API Gateway**

---

## ⚙️ Core Infrastructure Services

| Component     | Port | Technology                 | Responsibility                       |
| ------------- | ---- | -------------------------- | ------------------------------------ |
| API Gateway   | 8080 | Spring Cloud Gateway       | Routing, JWT validation, CORS        |
| Eureka Server | 8761 | Netflix Eureka             | Service discovery & registration     |
| Config Server | 8888 | Spring Cloud Config Server | Centralized configuration management |

---

## 🧩 Microservices Overview

| # | Service              | Port | Database   | Responsibility                     |
| - | -------------------- | ---- | ---------- | ---------------------------------- |
| 1 | User Service         | 8081 | PostgreSQL | Authentication, user profiles, JWT |
| 2 | Admin Service        | 8082 | PostgreSQL | Admin roles, dashboard             |
| 3 | Product Service      | 8083 | PostgreSQL | Books, categories, inventory       |
| 4 | Cart Service         | 8084 | Redis      | Cart management & calculations     |
| 5 | Wishlist Service     | 8085 | PostgreSQL | User wishlist                      |
| 6 | Customer Service     | 8086 | PostgreSQL | Addresses & preferences            |
| 7 | Order Service        | 8087 | PostgreSQL | Order processing, Kafka events     |
| 8 | Feedback Service     | 8088 | PostgreSQL | Reviews & ratings                  |
| 9 | Notification Service | 8089 | —          | Email/SMS via Kafka                |

---

## 🛠️ Technologies Used

* **Language:** Java 17
* **Framework:** Spring Boot 3.x
* **Microservices:** Spring Cloud
* **Service Discovery:** Netflix Eureka
* **API Gateway:** Spring Cloud Gateway
* **Security:** Spring Security + JWT
* **Messaging:** Apache Kafka
* **Databases:** PostgreSQL, Redis
* **Documentation:** Swagger / OpenAPI
* **Containerization:** Docker & Docker Compose
* **Orchestration:** Kubernetes (optional)
* **Build Tool:** Maven

---

## 📂 Project Structure

```
bookstore-microservices/
│
├── infrastructure/
│   ├── docker-compose.yml
│   ├── k8s/
│   └── scripts/
│
├── config-server/
├── eureka-server/
├── api-gateway/
│
├── services/
│   ├── user-service/
│   ├── admin-service/
│   ├── product-service/
│   ├── cart-service/
│   ├── wishlist-service/
│   ├── customer-service/
│   ├── order-service/
│   ├── feedback-service/
│   └── notification-service/
│
├── common-lib/
│   ├── dto/
│   ├── utils/
│   ├── exception/
│   └── security/
│
├── docs/
│   └── architecture.md
│
├── .github/workflows/
├── pom.xml
└── README.md
```

---

## 🐳 Deployment

* Each service is containerized using **Docker**
* Use **Docker Compose** for local development
* Supports **Kubernetes** for production deployment

---

## 📖 API Documentation

* Swagger UI available per service
* Can be aggregated via API Gateway

---

## 🔐 Security

* JWT-based authentication
* Secure endpoints using Spring Security
* Role-based access control

---

## 🔄 Communication Patterns

* **Synchronous:** REST APIs
* **Asynchronous:** Kafka events

---

## 🎯 Key Features

* Microservices-based architecture
* Independent service deployment
* Centralized configuration
* Service discovery
* API Gateway routing
* Event-driven communication
* Scalable & maintainable design

---

## 👩‍💻 Author

**Jayanthi**
Backend Developer | Java | Spring Boot | Microservices

---

## ⭐ Final Note

This project demonstrates **real-world backend architecture** used in enterprise systems and is designed to reflect **industry best practices** in microservices development.
